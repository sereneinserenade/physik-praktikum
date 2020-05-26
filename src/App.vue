<template>
  <v-app>
    <v-app-bar app color="green" dark>
      <v-btn href="/" target="_blank" text>
        <span class="mr-2">Mechanik Praktikum</span>
      </v-btn>
      <div></div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/sereneinserenade/physik-praktikum"
        target="_blank"
        text
      >
        <span class="mr-2">Zum Quellcode</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <v-container>
        <!-- Dialog Box-->
        <div class="text-center">
          <v-dialog v-model="dialog" width="500">
            <v-card>
              <v-card-title class="headline red lighten-1 " primary-title>
                Wir bedanken uns bei Ihnen.
              </v-card-title>

              <v-card-text class="mt-3">
                Lieber Herr Hornauer, <br />
                <br />
                wir bedanken uns bei Ihnen für so ein unfassbar tolles
                Praktikum. Wir haben die tollste Zeit gehabt, indem wir einfach
                versuchten, die Aufgaben gemeinsam zu lösen und zu verstehen und
                wie die Physik in der Welt eine größe Rolle spielt. Durch die
                Experimenten wurden uns klar, dass das Durchführen von
                Experimenten gar nicht leicht ist, aber mit Engagement kann man
                alles schaffen. Ich und mein Team wäre immer dafür dankbar.

                <div class="mt-3">
                  Mit ausgezeichneter Hochachtung, <br />
                  Jeet Mandaliya <br />
                  Nikhil Pingle <br />
                  Dmytro Shchurovskyi <br />
                  Grigori Nekhin
                </div>
              </v-card-text>

              <v-divider></v-divider>

              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="primary" text @click="dialogClose">
                  Zum Protokoll
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
        </div>
      </v-container>

      <v-container>
        <main class="mainCss" v-if="showMain">
          <v-expansion-panels class="expPanelsClass">
            <!--            aufgabe 1-->
            <v-expansion-panel class="expPanelClass">
              <v-expansion-panel-header
                >Aufgabe 1: Besenstiel</v-expansion-panel-header
              >
              <v-expansion-panel-content>
                <div class="frage">
                  Frage : Sie bewegen einen Auflagepunkt langsam
                  („quasistatisch“) und gleichmäßig zum anderen.
                  X(t)=X<sub>0</sub>-V<sub>0</sub>·t. Erläutern Sie warum immer
                  0&lt;S(t)&lt;X(t) gilt. Berechnen und messen Sie die Bewegung
                  des Schwerpunktes S(t). Erstellen sie Diagramme für S(t) und
                  S(t) und versuchen Sie eine Theorie- kurve grob anzupassen.
                  EXTRA: Wie sieht S(t) ohne diese quasistatische Näherung –
                  d.h. bei großem V<sub>0</sub> aus?
                </div>
                <div
                  class="headline d-flex align-content-center justify-center mt-5"
                >
                  <div>
                    Antwort
                  </div>
                </div>
                <div class="antwort mt-5">
                  <div class="d-flex align-content-space-between">
                    <div>
                      <video-player class="videoThing" style="width: 50%;">
                        <source src="../src/assets/videos/dimaAufEins.mp4" />
                      </video-player>
                      Video von Dmytro Shchurovskyi
                    </div>
                    <div class="explain" style="width: 50%">
                      Die Erklärung findet hier staat.
                    </div>
                  </div>
                </div>
                <div class="extraAns mt-5">
                  Beim großen V<sub>0</sub> kann zwischen Objekt und
                  Auflagerpunkt B keine Haftreibung entstehen weil diese Kraft
                  nur zwischen nicht bewegende Objekte entstehet, deswegen
                  bleibt Auflager B bewegen bezüglich Objekte, und wenn es durch
                  schwerpunkt kommt, kippt Das System um
                </div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <!--            aufgabe 2-->
            <v-expansion-panel class="expPanelClass">
              <v-expansion-panel-header
                >Aufgabe 2: Getränkedose</v-expansion-panel-header
              >
              <v-expansion-panel-content>
                <div class="frage">
                  Kaufen Sie ein Dose mit einem Getränk Ihrer Wahl. Bestimmen
                  Sie den Schwerpunkt der vollen Dose. Kippen Sie die Dose, bis
                  der momentane Schwerpunkt über dem Auflagepunkt liegt.
                  Bestimmen sie den Gleichgewichtswinkel Φ<sub>0</sub> Leeren
                  Sie die Dose systematisch und bestimmen Sie den jeweiligen
                  Gleichgewichtswinkel Φ(h) in Abhängigkeit der Füllhöhe h.
                  Berechen Sie die Höhe des Schwerpunktes, wenn die Dose
                  senkrecht steht. Bei welchen Füllhöhen hG steht die Dose
                  stabil auf dem Rand? Erstellen Sie ein Diagramm für Φ(h) und
                  zeichnen Sie den Bereich für hG ein.
                </div>
                <div
                  class="headline d-flex align-content-center justify-center mt-5"
                >
                  <div>
                    Antwort
                  </div>
                </div>
                <div class="antwort"></div>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <!--            aufgabe 3 -->
            <v-expansion-panel class="expPanelClass">
              <v-expansion-panel-header
                >Aufgabe 3: Bücherstapel</v-expansion-panel-header
              >
              <v-expansion-panel-content>
                <div class="frage">
                  Stapeln Sie Dinge lose übereinander, sodass ein möglichst
                  großer Überstand ΔΣ entsteht. Leiten Sie die Beziehung Δn in
                  der idealen Welt her: <br />
                  <br />

                  1. alle Bücher exakt gleich, 2. beliebig scharfe Kanten 3.
                  beliebig viele Bücher vorhanden, 4. alles statisch. 5. Bücher
                  und Tisch beliebig stabil <br />
                  <br />

                  Und in der fast idealen Welt: <br />
                  6. Zur Sicherheit wird jedes Buch um einen konstanten
                  Bruchteil ε=2% der Länge Li zurückgeschoben. <br />
                  <br />

                  Wie groß kann ΔΣ in beiden Welten maximal werden?
                </div>
                <div
                  class="headline d-flex align-content-center justify-center mt-5"
                >
                  <div>
                    Antwort
                  </div>
                </div>
                <div class="antwort">
                  Δ<sub>Σ</sub> = möglicht großer Überstand, M = Masse eines
                  Buches <br />
                  <br />

                  Der Hitergrundgedanke : Der schwerpunkt von n Büchern soll
                  genau am Ende des Tisches liegen. Dabei soll man aber auch
                  darüber nachdenken, daß der Schwerpunkt von n - 1 Bücher
                  direkt über der Vorderkante des unteren Buches liegt. <br />
                  <br />

                  Die Rechnung is bezüglich der Länge des Buches. <br />
                  <br />

                  <p>
                    Vergleichen der Momente der Bücher
                    <img
                      src="../src/assets/Bildschirmfoto 2020-05-26 um 03.14.02.png"
                      style="width: 100%;"
                    />
                    Daraus folgt
                    <img
                      src="../src/assets/Bildschirmfoto 2020-05-26 um 03.14.31.png"
                      style="width: 100%;"
                    />
                    Mit weiterer Rechnung
                    <img
                      src="../src/assets/Bildschirmfoto 2020-05-26 um 03.14.37.png"
                      style="width: 100%;"
                    />
                    <img
                      src="../src/assets/Bildschirmfoto 2020-05-26 um 03.14.41.png"
                      style="width: 100%;"
                    />
                    <img
                      src="../src/assets/Bildschirmfoto 2020-05-26 um 03.14.44.png"
                      style="width: 100%;"
                    />
                  </p>

                  <p>
                    Bei der Prüfung dieser Formel kommt mit n=1 d<sub>n</sub> =
                    0.5 raus. Das heißt, daß ein halbes Buch soll auf dem Tisch
                    bleiben.
                  </p>
                </div>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </main>
      </v-container>
    </v-content>

    <!-- for the confettis -->
    <div class="myBtn">
      <v-btn v-if="!notConf" @click="start">
        <span class="mr-2">Confetti Wieder Starten</span>
        <v-icon>mdi-play</v-icon>
      </v-btn>
      <v-btn v-else @click="stop">
        <span class="mr-2">Confetti Beenden</span>
        <v-icon class="rotated">mdi-plus</v-icon>
      </v-btn>
    </div>
  </v-app>
</template>

<script>
import { videoPlayer } from "vue-md-player";
import "vue-md-player/dist/vue-md-player.css";

export default {
  name: "App",

  components: {
    videoPlayer
  },

  data: () => ({
    showMain: false,
    dialog: true,
    showConfetti: false,
    notConf: false
  }),

  created() {
    this.$vuetify.theme.dark = true;
  },

  methods: {
    dialogClose() {
      this.dialog = false;
      this.showConfetti = true;
      this.start();
      this.showMain = !this.showMain;
    },
    start() {
      this.$confetti.start({
        particlesPerFrame: 0.5
      });
      this.notConf = !this.notConf;
    },

    stop() {
      this.$confetti.stop();
      this.notConf = !this.notConf;
    },

    love() {
      this.$confetti.update({
        particles: [
          {
            type: "heart"
          },
          {
            type: "circle"
          }
        ],
        defaultColors: ["red", "pink", "#ba0000"]
      });
    }
  }
};
</script>
<style>
.rotated {
  transform: rotate(45deg);
}
.myBtn {
  position: fixed;
  bottom: 2em;
  right: 2em;
}
.mainCss {
  background: rgba(256, 256, 256, 0.1);
}
.frage {
  color: darkorange;
}
.frage::first-letter {
  font-size: 1.5em;
}
.extraAns {
  color: aquamarine;
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
}
.videoThing {
  height: 70vh;
}
</style>
