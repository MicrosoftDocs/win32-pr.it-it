---
description: In TAPI versione 3.0 e successive, il modello a oggetti TAPI usa oggetti terminali per rappresentare l'origine o il sink di un flusso multimediale associato a una sessione di chiamata o di comunicazione.
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Oggetto terminale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe85dcf2643cbf60835a7df9e8b20de8287da2c752ed6555f480609d9b79873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476261"
---
# <a name="terminal-object"></a>Oggetto terminale

In TAPI versione 3.0 e successive, il modello a oggetti TAPI usa oggetti terminali per rappresentare l'origine o il sink di un flusso multimediale associato a una sessione di chiamata o di comunicazione. Questo modello a oggetti consente a un'applicazione di specificare, a livello dettagliato, la modalità di elaborazione dei supporti in una chiamata. Questo modello consente anche di selezionare più terminali contemporaneamente, quindi, ad esempio, una chiamata può essere restituita a un altoparlante audio e registrata contemporaneamente.

L'oggetto Terminale rappresenta un'origine o un renderer, ad esempio un microfono o un altoparlante. Un'applicazione sceglie tra i terminali disponibili in base alla direzione dei supporti e al tipo o ai tipi coinvolti in una sessione di comunicazione. Ogni flusso multimediale associato viene quindi selezionato nel terminale appropriato per avviare lo streaming.

I terminali vengono in genere implementati da un provider di servizi multimediali (MSP) e gli oggetti terminale non saranno disponibili se non è presente alcun msp associato a una sessione di comunicazione. Un'eccezione è che con Windows 2000 SP1 e versioni successive, un'applicazione può implementare una forma di [terminale collegabile.](pluggable-terminals.md) In questo modo un server di conferenza può creare terminali di bridging in modo che i client non Windows 2000 SP1 o non multicast H323 possano essere aggiunti alle conferenze multicast SDP/IP TAPI 3 multi-party.

Ogni terminale appartiene a una [classe terminale](terminal-class.md). Una classe terminale rappresenta un set di funzionalità di origine o di rendering. Ad esempio, un terminale che esegue il mapping a un set di altoparlanti audio verrebbe identificato come CLSID SpeakersTerminal e il provider di servizi dovrebbe implementare il controllo \_ del volume. TAPI 3 definisce un set di classi terminale, un msp può definire classi aggiuntive e un'applicazione può registrare nuove classi terminale. A ogni classe terminale viene assegnato un identificatore univoco globale (GUID).

Dal punto di vista di un'applicazione, un terminale è descritto dal tipo [e](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) dalla direzione del [terminale.](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) Il tipo può essere statico o dinamico. Un terminale statico esegue il mapping all'hardware, ad esempio un telefono o un microfono. Un terminale dinamico esegue il mapping a un oggetto temporaneo, ad esempio un file o una finestra video. La direzione indica se un terminale specificato è un'origine o un renderer.

Le funzionalità di un determinato oggetto terminale possono variare notevolmente a seconda della coppia di provider di servizi corrente in uso. Il msp per un dispositivo specializzato potrebbe implementare un'interfaccia con i metodi appropriati per tale dispositivo. Tale interfaccia può essere aggregata nell'oggetto terminale e i metodi resi disponibili per un'applicazione. Per altre informazioni e materiale di riferimento, vedere la documentazione del provider di servizi multimediali.

Per altre informazioni sulle interfacce terminali e sui metodi implementati da TAPI 3, vedere [Terminal Object Interfaces](terminal-object-interfaces.md).

Se gli autori di un provider di servizi multimediali usano le classi di base MSP, possono implementare alcune delle funzionalità di Terminale di streaming multimediale.

Per altre informazioni ed esempi di codice che illustrano le illustrazioni dell'uso di un oggetto Terminal, vedere [Effettuare](make-a-call.md) una chiamata [e ricevere una chiamata](receive-a-call.md).

**Windows XP:** Per altre informazioni su come l'oggetto Terminale è stato espanso in Windows XP, vedere [Terminali file,](file-terminals.md) [terminali multitraccia](multitrack-terminals.md)e [terminali collegabili.](pluggable-terminals.md)

Per altre informazioni ed esempi di codice, vedere Uso di [terminali file](using-file-terminals.md), Uso di [terminali multitraccia](using-multitrack-terminals-and-the-default-selection-mechanism.md)e meccanismo di selezione predefinito e Registrazione [del terminale collegabile](pluggable-terminal-registration.md).

 

 



