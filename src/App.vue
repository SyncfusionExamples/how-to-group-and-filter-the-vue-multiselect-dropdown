<template>
    <div>
      <div style="margin:10% 40%; width:250px;">
        <ejs-multiselect popupHeight="200px" popupWidth="250px" 
        :dataSource='dataItem' :fields='dataFields' 
        placeholder='Select a vegetable' :allowFiltering='true'
        :ignoreCase='false' filterType='Contains' enableGroupCheckBox='true'
        mode='CheckBox'>
        </ejs-multiselect>
        <!-- <ejs-multiselect popupHeight="200px" popupWidth="250px" 
        :dataSource='dataItem' :fields='dataFields' 
        placeholder='Select a value' :allowFiltering='true'
        :ignoreAccent='true' enableGroupCheckBox='true'
        mode='CheckBox'>
        </ejs-multiselect> -->
      </div>
    </div>
</template>

<script>
import Vue from "vue";
import { MultiSelectPlugin, MultiSelect,CheckBoxSelection } from "@syncfusion/ej2-vue-dropdowns";
Vue.use(MultiSelectPlugin);
MultiSelect.Inject(CheckBoxSelection);
export default Vue.extend({
  data: function() {
    return {
      //  dataItem : [
      //       'Aeróbics',
      //       'Aeróbics en Agua',
      //       'Aerografía',
      //       'Aeromodelaje',
      //       'Águilas',
      //       'Ajedrez',
      //       'Ala Delta',
      //       'Álbumes de Música',
      //       'Alusivos',
      //       'Análisis de Escritura a Mano'
      //   ],
      dataItem: [
        { Name: 'Cabbage', Category: 'Leafy and Salad', Id: 'item1' },
        { Name: 'Spinach', Category: 'Leafy and Salad', Id: 'item2' },
        { Name: 'Wheat grass', Category: 'Leafy and Salad', Id: 'item3' },
        { Name: 'Yarrow', Category: 'Leafy and Salad', Id: 'item4' },
        { Name: 'Pumpkins', Category: 'Leafy and Salad', Id: 'item5' },
        { Name: 'Chickpea', Category: 'Beans', Id: 'item6' },
        { Name: 'Green bean', Category: 'Beans', Id: 'item7' },
        { Name: 'Horse gram', Category: 'Beans', Id: 'item8' }
        ],
      dataFields: { 
        groupBy: 'Category', 
        text: 'Name', 
        value: 'Id' }
     }
  }
});

</script>
<style>
@import url(https://cdn.syncfusion.com/ej2/material.css);
</style>