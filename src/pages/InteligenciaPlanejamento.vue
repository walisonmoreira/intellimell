<template>
  <q-page padding>
    <div class="row q-col-gutter-md">
      <div class="col-xs-12 col-sm-6 col-md-4">
        <q-card>
          <q-img src="/statics/vendas.png">
            <div class="absolute-bottom">
              <div class="text-h6">Vendas do Produto Principal</div>
              <div>Gerar inteligência a fim de ajudar a vender ao menos 200.000 caixas do produto principal no primeiro ano.</div>
            </div>
          </q-img>
          <q-card-actions>
            <q-btn flat @click="alerta = true">Editar</q-btn>
            <q-btn flat @click="alerta = true">FCS</q-btn>
            <q-btn flat @click="alerta = true">Ajuda</q-btn>
          </q-card-actions>
        </q-card>
      </div>
      <div class="col-xs-12 col-sm-6 col-md-4">
        <q-card>
          <q-img src="/statics/logistica.png">
            <div class="absolute-bottom">
              <div class="text-h6">Software de Logística</div>
              <div>Gerar inteligência a fim de ajudar a adquirir o software de logística e treinar as equipes até fevereiro de 2020.</div>
            </div>
          </q-img>
          <q-card-actions>
            <q-btn flat @click="alerta = true">Editar</q-btn>
            <q-btn flat @click="alerta = true">FCS</q-btn>
            <q-btn flat @click="alerta = true">Ajuda</q-btn>
          </q-card-actions>
        </q-card>
      </div>
      <div class="col-xs-12 col-sm-6 col-md-4">
        <q-card>
          <q-img src="/statics/marketing.png">
            <div class="absolute-bottom">
              <div class="text-h6">Marketing e Comunicação</div>
              <div>Gerar inteligência a fim de ajudar a desenvolver toda campanha de marketing e comunicação até março de 2020.</div>
            </div>
          </q-img>
          <q-card-actions>
            <q-btn flat @click="alerta = true">Editar</q-btn>
            <q-btn flat @click="alerta = true">FCS</q-btn>
            <q-btn flat @click="alerta = true">Ajuda</q-btn>
          </q-card-actions>
        </q-card>
      </div>
      <div class="col-xs-12 col-sm-6 col-md-4">
        <q-card>
          <q-img src="/statics/exportacao.png">
            <div class="absolute-bottom">
              <div class="text-h6">Manual de Exportação</div>
              <div>Gerar inteligência a fim de ajudar a construir um manual de exportação para a China redigido e revisado até março de 2020.</div>
            </div>
          </q-img>
          <q-card-actions>
            <q-btn flat @click="alerta = true">Editar</q-btn>
            <q-btn flat @click="alerta = true">FCS</q-btn>
            <q-btn flat @click="alerta = true">Ajuda</q-btn>
          </q-card-actions>
        </q-card>
      </div>
    </div>
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
  </q-page>
</template>

<script>
export default {
  name: 'PageInteligenciaPlanejamento',
  data () {
    return {
      alerta: false
    }
  }
}
</script>
