<template>
   <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                <h5 class="modal-title" id="exampleModalLabel">{{character.name}}</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <div class="col-md-12">
                      <img :src="character.thumbnail" class="img-fluid rounded-start" :alt="character.name">
                    </div>
                    <div class="col-md-12">
                      <p class="text-muted">{{character.modified}}</p>
                      <h3>
                        Описание
                      </h3>
                      <p>
                        {{character.description}}
                      </p>
                      <h3>
                        Комиксы:
                      </h3>
                        <ul>
                          <li
                            v-for="(el, idx) in character.comics"
                            :key="idx"
                          >
                            {{el.name}}
                          </li>
                        </ul>
                    </div>
                </div>
                <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Закрыть</button>
                </div>
            </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "AppModal",
        props: ['character']
    }
</script>

<style scoped>

</style>
