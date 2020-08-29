<template>
  <el-dialog type="warning" title="Διαχείριση Προμηθευτή" :visible="visible" :modal="true"
             :close-on-click-modal="false"
             :close-on-press-escape="false" :modal-append-to-body="false" :show-close="false" width="75%"
             @close="clearValidation">

    <el-card>
    <el-form ref="supplierForm" :model="supplier" :rules="rules" label-position="top">

      <el-row :gutter="20">
        <!-- LEFT COLUMN -->
        <el-col :span="12">

          <el-form-item label="Εισάγετε το όνομα"
                        prop="firame">
            <el-input prefix-icon="fa fa-user"
                      v-model="supplier.firstName"
                      placeholder="Όνομα"
                      autoComplete="frstName">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε το επώνυμο"
                        prop="lastName">
            <el-input prefix-icon="fa fa-user"
                      v-model="supplier.lastName"
                      placeholder="Επώνυμο"
                      autoComplete="lastName">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε τη διεύθυνση"
                        prop="address">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.address"
                      type="address"
                      placeholder="Address"
                      autoComplete="address">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε το ταχυδρομικό κώδικα"
                        prop="zipCode">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.zipCode"
                      type="zipCode"
                      placeholder="ZIP Code"
                      autoComplete="zipCode">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε την πόλη"
                        prop="city">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.city"
                      type="city"
                      placeholder="City"
                      autoComplete="city">
            </el-input>
          </el-form-item>

        </el-col>

        <!-- RIGHT COLUMN -->
        <el-col :span="12">

          <el-form-item label="Εισάγετε την χώρα"
                        prop="country">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.country"
                      type="country"
                      placeholder="Country"
                      autoComplete="country">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε το όνομα της εταιρείας"
                        prop="companyName">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.companyName"
                      type="companyName"
                      placeholder="companyName"
                      autoComplete="companyName">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε το IRS γραφείο"
                        prop="irsOffice">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.irsOffice"
                      type="irsOffice"
                      placeholder="IRS Office"
                      autoComplete="irsOffice">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε το VAT νούμερο"
                        prop="vatNumber">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.vatNumber"
                      type="vatNumber"
                      placeholder="VAT Number"
                      autoComplete="vatNumber">
            </el-input>
          </el-form-item>

        </el-col>
      </el-row>

    </el-form>

      <el-row>
        <el-col style="text-align: right">
          <el-button type="success"
                     icon="fa fa-save"
                     @click="save"> Αποθήκευση </el-button>

          <el-button type="danger"
                     icon="fa fa-remove"
                     @click="confirmDelete"
                     :disabled="!isDeletable"> Διαγραφή </el-button>
        </el-col>
      </el-row>
    </el-card>

    <div slot="footer" class="dialog-footer card-footer">
      <el-button type="warning"
                 icon="el-icon-back"
                 @click="cancel"> Επιστροφή </el-button>
    </div>

  </el-dialog>
</template>
<script src="./SupplierVM.js"></script>
