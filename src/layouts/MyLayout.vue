<template>
  <q-layout view="hHh LpR fFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn flat dense round icon="menu" @click="left = !left"/>
        <q-toolbar-title>IntelliMell</q-toolbar-title>
        <q-btn @click="alerta = true" flat round dense icon="more_vert" />
      </q-toolbar>
    </q-header>
    <q-drawer bordered behavior="mobile" v-model="left">
      <q-list>
        <q-item-label header>Projetos de Inteligência</q-item-label>
        <q-item to="/inteligencia-planejamento">
          <q-item-section avatar>
            <q-icon name="assignment"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Inteligência de Planejamento</q-item-label>
            <q-item-label caption>Apoiar o alcance de metas</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable @click="alerta = true">
          <q-item-section avatar>
            <q-icon name="visibility"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Inteligência de Vigilância</q-item-label>
            <q-item-label caption>Maximizar oportunidades e mitigar riscos</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable @click="alerta = true">
          <q-item-section avatar>
            <q-icon name="local_hospital"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Inteligência de Suporte</q-item-label>
            <q-item-label caption>Definição de diretrizes e metas estratégicas</q-item-label>
          </q-item-section>
        </q-item>
        <q-item-label header>Configurações</q-item-label>
        <q-item to="/exportar-importar">
          <q-item-section avatar>
            <q-icon name="swap_vertical_circle"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Exportar/Importar</q-item-label>
            <q-item-label caption>Excel, Google Planilhas, PDF...</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable @click="alerta = true">
          <q-item-section avatar>
            <q-icon name="security"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Segurança</q-item-label>
            <q-item-label caption>Usuários, controle de acesso, ...</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable @click="alerta = true">
          <q-item-section avatar>
            <q-icon name="chat"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Suporte</q-item-label>
            <q-item-label caption>Chat, e-mail, ticket, forum, ...</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable @click="alerta = true">
          <q-item-section avatar>
            <q-icon name="help"/>
          </q-item-section>
          <q-item-section>
            <q-item-label>Ajuda</q-item-label>
            <q-item-label caption>Manuais, guias, dúvidas, ...</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>
    <q-page-container>
      <router-view/>
    </q-page-container>
    <q-dialog v-model="alerta">
      <q-card>
        <q-card-section>
          <div class="text-h6">Atenção!</div>
        </q-card-section>
        <q-card-section>
          Essa funcionalidade ainda não está pronta.
        </q-card-section>
        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MainLayout',
  data () {
    return {
      left: this.$q.platform.is.desktop,
      alerta: false
    }
  },
  methods: {
    openURL
  }
}
</script>
