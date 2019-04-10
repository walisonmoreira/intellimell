<template>
  <q-page padding>
    <div class="row q-col-gutter-md">
      <div class="col-xs-12 col-sm-6 col-md-4">
        <q-card>
          <q-img src="statics/excel.png">
            <div class="absolute-bottom">
              <div class="text-h6">Integração com o Microsoft Excel</div>
              <div class="text-subtitle2">Veja e altere seus projetos direto na planíliha</div>
            </div>
          </q-img>
          <q-card-actions>
            <q-btn flat @click="alerta = true">Exportar</q-btn>
            <q-btn flat @click="alerta = true">Importar</q-btn>
          </q-card-actions>
        </q-card>
      </div>
      <div class="col-xs-12 col-sm-6 col-md-4">
        <q-card>
          <q-img src="statics/google-sheets.png">
            <div class="absolute-bottom">
              <div class="text-h6">Integração com o Google Planilhas</div>
              <div class="text-subtitle2">Projetos de inteligência na núvem do Google</div>
            </div>
          </q-img>
          <q-card-actions>
            <q-btn flat @click="alerta = true">Exportar</q-btn>
            <q-btn flat @click="alerta = true">Importar</q-btn>
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
  name: 'PageExportarImportar',
  data () {
    return {
      alerta: false
    }
  }
}
</script>
