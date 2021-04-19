---
description: In TAPI versione 3,0 e versioni successive, il modello a oggetti TAPI usa gli oggetti terminal per rappresentare l'origine o il sink di un flusso multimediale associato a una chiamata o a una sessione di comunicazione.
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Oggetto terminale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2568d3c6f047fec8ca46b3b7d56e5026b61a1113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319850"
---
# <a name="terminal-object"></a>Oggetto terminale

In TAPI versione 3,0 e versioni successive, il modello a oggetti TAPI usa gli oggetti terminal per rappresentare l'origine o il sink di un flusso multimediale associato a una chiamata o a una sessione di comunicazione. Questo modello a oggetti consente a un'applicazione di specificare, a un livello dettagliato, il modo in cui vengono elaborati i supporti in una chiamata. Questo modello consente inoltre la selezione simultanea di più terminali. ad esempio, una chiamata può essere restituita a un altoparlante audio e registrata simultaneamente.

L'oggetto terminale rappresenta un'origine o un renderer, ad esempio un microfono o un altoparlante. Un'applicazione sceglie tra i terminali disponibili in base alla direzione del supporto e al tipo o ai tipi necessari in una sessione di comunicazione. Ogni flusso multimediale associato viene quindi selezionato sul terminale appropriato per poter avviare lo streaming.

I terminali vengono in genere implementati da un provider di servizi multimediali (MSP) e gli oggetti terminal non saranno disponibili se non è presente alcun MSP associato a una sessione di comunicazione. Un'eccezione è che con Windows 2000 SP1 e versioni successive, un'applicazione può implementare una forma di [terminale innestabile](pluggable-terminals.md). Questo consente a un server di conferenza di creare terminali di bridging in modo che i client non Windows 2000 SP1 o non multicast H323 possano essere aggiunti a conferenze multicast SDP/IP multiparte di TAPI 3.

Ogni terminale appartiene a una [classe terminale](terminal-class.md). Una classe Terminal rappresenta un set di funzionalità di origine o di rendering. Ad esempio, un terminale che esegue il mapping a un set di altoparlanti audio viene identificato come CLSID \_ SpeakersTerminal e il provider di servizi dovrebbe implementare il controllo del volume. TAPI 3 definisce un set di classi Terminal, un MSP può definire classi aggiuntive e un'applicazione può registrare nuove classi terminal. A ogni classe terminal viene assegnato un identificatore univoco globale (GUID).

Dal punto di vista di un'applicazione, un terminale viene descritto dal tipo e dalla [direzione](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)del [terminale](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) . Il tipo può essere statico o dinamico. Un terminale statico viene mappato a hardware, ad esempio un telefono o un microfono. Un terminale dinamico viene mappato a un oggetto temporaneo, ad esempio un file o una finestra video. Direction indica se un determinato terminale è un'origine o un renderer.

Le funzionalità di un determinato oggetto terminale possono variare notevolmente a seconda della coppia di provider di servizi corrente in uso. Il MSP per un dispositivo specializzato potrebbe implementare un'interfaccia con i metodi appropriati per il dispositivo. Tale interfaccia può essere aggregata nell'oggetto terminale e i metodi resi disponibili per un'applicazione. Per ulteriori informazioni e materiale di riferimento, vedere la documentazione del provider di servizi multimediali.

Per altre informazioni sulle interfacce terminali e sui metodi implementati da TAPI 3, vedere [interfacce di oggetti terminali](terminal-object-interfaces.md).

Se gli autori di un provider di servizi multimediali utilizzano le classi di base MSP, possono implementare alcune delle funzionalità del terminale di streaming multimediale.

Per ulteriori informazioni ed esempi di codice in cui vengono illustrate le illustrazioni dell'utilizzo di un oggetto terminale, vedere [effettuare una chiamata](make-a-call.md) e [ricevere una chiamata](receive-a-call.md).

**Windows XP:** Per ulteriori informazioni sulla modalità di espansione dell'oggetto terminale in Windows XP, vedere [terminali di file](file-terminals.md), [terminali multitraccia](multitrack-terminals.md)e [terminali collegabili](pluggable-terminals.md).

Per altre informazioni ed esempi di codice, vedere [uso di terminali di file](using-file-terminals.md), uso di [terminali multitraccia e il meccanismo di selezione predefinito](using-multitrack-terminals-and-the-default-selection-mechanism.md)e [registrazione di terminali collegati](pluggable-terminal-registration.md).

 

 



