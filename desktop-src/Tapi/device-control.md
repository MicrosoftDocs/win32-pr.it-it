---
description: Il controllo del dispositivo a livello di utente finale o di applicazione server richiede un set relativamente ridotto di informazioni di base.
ms.assetid: 9c787656-93ef-4e0b-9516-8822ae49a83a
title: Controllo dispositivo (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f67b33cb03b5a4ac84309bd9c463a9d73e1ebfb8bf51deb4189585f9e1ec3752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867403"
---
# <a name="device-control-telephony-api"></a>Controllo dispositivo (API di telefonia)

Il controllo del dispositivo a livello di utente finale o di applicazione server richiede un set relativamente ridotto di informazioni di base. Il livello di astrazione del provider di servizi esegue il controllo dettagliato del dispositivo. I provider di servizi segnalano le informazioni sul dispositivo necessarie a un'applicazione tramite TAPI.

Le categorie di dispositivi principali includono:

-   [Rete:](network-ovr.md)livello di trasporto per le comunicazioni. Dal punto di vista di un'applicazione, le informazioni sulla rete vengono in genere incorporate nel tipo di indirizzo, ad esempio LINEADDRESSTYPE \_ PHONENUMBER.
-   [Riga:](line-ovr.md)connessione a una rete. Questo concetto è ampiamente usato all'interno di TAPI 2.2 (TAPI/C).
-   [Channel:](channel-ovr.md)suddivisione di una linea. La conoscenza dei canali in genere non è necessaria per un'applicazione perché il provider di servizi configura la modalità di visualizzazione come indirizzi.
-   [Indirizzo:](address-ovr.md)un percorso di rete in una rete. A ogni riga o canale sono associati uno o più indirizzi. L'indirizzo è un concetto chiave sia in TAPI 3.1 (TAPI/COM) che in TAPI 2.2 (TAPI/C).
-   [Terminale:](terminal-ovr.md)origine o renderer per un indirizzo e un tipo di supporto specifici.

I provider di servizi segnalano le caratteristiche del dispositivo a TAPI in risposta alle query dell'applicazione. I provider di servizi avviano anche report sulle modifiche apportate allo stato del dispositivo. Queste modifiche vengono quindi segnalate a un'applicazione in base alle notifiche richieste durante l'inizializzazione.

Le caratteristiche di base del dispositivo sono:

-   [Classe Device](device-class-ovr.md)
-   [Identificatore del dispositivo](device-identifier-ovr.md)
-   [Tipo di indirizzo](address-type-ovr.md)
-   [Identificatore indirizzo](address-identifier-ovr.md)
-   [Eventi del dispositivo](device-events-ovr.md)
-   [Tipo di supporto](media-type-ovr.md)
-   [Tipo di terminale](terminal-type-ovr.md)

Inoltre, i provider di servizi forniscono informazioni relative alla capacità di un determinato indirizzo di eseguire varie operazioni di sessione.

Le caratteristiche supplementari possono essere associate a determinati dispositivi, se i provider di servizi li supportano. Un'applicazione TAPI 2.x individua le funzionalità usando le funzioni [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) e [**lineGetAddressCaps.**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) Le applicazioni TAPI 3.x usano [**l'interfaccia ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) a questo scopo.

TAPI 2.x offre un set speciale di operazioni supplementari che il provider di servizi può implementare per l'uso con i dispositivi telefonici. Vedere [Telefono dispositivi .](./opening-and-closing-phone-devices.md)

Le funzionalità estese sono specifiche del provider e non sono coperte direttamente dall'API di telefonia Microsoft. Vedere [Funzioni di linea estese,](./extended-line-functions.md) [Telefonia Telefono funzioni](./extended-telephony-phone-functions.md)o interfacce specifiche del [provider.](provider-specific-interfaces.md)

Di seguito è riportato un riepilogo delle operazioni TAPI che e consentono di eseguire query sui provider di servizi sulle caratteristiche del dispositivo e di fornire dati sullo stato corrente.



| Funzioni TAPI 2.x                                                  | Descrizione                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)                   | Esegue una query su un dispositivo linea specificato per determinare le funzionalità di telefonia degli indirizzi associati.               |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)           | Esegue una query su un dispositivo linea specificato per determinare le funzionalità di telefonia di un indirizzo specifico.                   |
| [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig)               | Restituisce una struttura di dati "opaca" che archivia la configurazione corrente di un dispositivo.                          |
| [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig)               | Ripristina la configurazione del dispositivo.                                                                                 |
| [**Finestra di dialogo lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog)               | Visualizzare una finestra di dialogo che consente all'utente di configurare i parametri correlati al dispositivo.                       |
| [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid)                             | Recupera un identificatore di dispositivo stabile che può essere usato in altre chiamate di funzione TAPI o con un'API diversa. |
| [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)       | Esegue una query sul dispositivo per lo stato corrente, ad esempio il numero di chiamate attive.                                             |
| [**lineSetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linesetlinedevstatus)       | Imposta lo stato del dispositivo, ad esempio l'impostazione di un dispositivo come non in servizio.                                                |
| [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon)                         | Recupera l'icona specifica del provider per la visualizzazione all'utente.                                                      |
| [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) | Consente a un'applicazione di negoziare una versione dell'estensione da usare con il dispositivo a linee specificato.                 |
| [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)                 | Consente l'accesso alle funzionalità specifiche del dispositivo.                                                                      |
| [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)   | Invia funzionalità specifiche del dispositivo al provider di servizi.                                                        |



 



| Interfacce o metodi TAPI 3.x                                   | Descrizione                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)           | Ottiene informazioni relative alle funzionalità di un indirizzo.                                                  |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                       | Imposta e ottiene DirectShow™ formato multimediale.                                                                 |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)             | Imposta e ottiene le caratteristiche del terminale audio standard, ad esempio il volume.                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                         | Ottiene informazioni relative alle funzionalità di supporto multimediale di un indirizzo.                                    |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                 | Interfaccia di base per l'oggetto Terminal. Ottiene informazioni come la classe terminale e i supporti supportati. |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                   | Ottiene informazioni sui terminali disponibili e crea terminali aggiuntivi.                               |
| [Interfacce specifiche del provider](provider-specific-interfaces.md) | Dipendente dal provider di servizi.                                                                             |



 

 

 
