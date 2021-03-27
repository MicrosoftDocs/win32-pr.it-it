---
description: Di seguito vengono fornite informazioni sulle scelte da tenere in considerazione quando si adattano i riquadri delle app desktop per Windows 8, tra cui come progettare riquadri delle app desktop per la nuova schermata Start e come scegliere i punti di ingresso da visualizzare nella schermata Start.
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: Riquadri delle app desktop nella schermata Start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcc5475732926300e2125ae9e97ea2d188bc468
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350981"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a>Riquadri delle app desktop nella schermata Start

Di seguito vengono fornite informazioni sulle scelte da tenere in considerazione quando si adattano i riquadri delle app desktop per Windows 8, tra cui come progettare riquadri delle app desktop per la nuova schermata Start e come scegliere i punti di ingresso da visualizzare nella schermata Start.

## <a name="design-your-tile-for-the-start-screen"></a>Progettare il riquadro per la schermata Start

È possibile personalizzare due aspetti dei riquadri dell'app desktop: il nome dell'app e l'icona. Il colore di sfondo è derivato dal colore di sfondo scelto dall'utente e non è personalizzabile a livello di codice.

![linee guida per la progettazione di un riquadro dell'app.](images/tiles-desktop-1.png)

DO: evitare il troncamento del nome dell'applicazione. I riquadri del desktop aggiunti alla schermata Start possono contenere fino a due righe di testo ciascuna riga o circa dieci caratteri (anche se dipende dalla lingua dell'interfaccia utente), quindi provare a tenere il nome dell'applicazione abbastanza breve da evitare il troncamento.

DO: fornire icone per i quattro valori di scala della schermata Start supportati per assicurarsi che le icone risultino nitide per tutti i fattori di forma.



| Scalabilità | Dimensioni riquadro (in pixel) | Dimensioni icone utilizzate (in pixel) |
|-------|-----------------------|----------------------------|
| 80%   | 120 x 120             | 48 x 48                    |
| 100%  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

DO: adottare i principi di progettazione Microsoft. Il nuovo aspetto delle icone è Flat, quindi se si vuole imitare le icone delle app di Windows Store per l'app desktop, prendere in considerazione l'eliminazione di ombre e così via.

No: evitare di usare il colore. Sebbene le icone delle app di Windows Store siano a volte monocromatiche, è consigliabile usare icone di colore per le app desktop. Questo consente di distinguere le applicazioni desktop sulla barra delle applicazioni e da altri riquadri dell'app desktop nella schermata Start perché il colore di sfondo dei riquadri desktop non può essere personalizzato. Prendere in considerazione l'uso di colori più saturi.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Decidere i punti di ingresso corretti da includere nella schermata Start

DO: aggiungere un collegamento per ogni app nella schermata Start quando viene installata l'app. Ciò garantisce che gli utenti possano avviare l'app direttamente dalla schermata Start o tramite la ricerca. Se non si include un collegamento nella schermata Start, l'avvio dell'app diventa difficile. In particolare, non aggiungere un collegamento solo sul desktop. Quando si accede per la prima volta, gli utenti visualizzano la schermata Start e quindi l'inserimento di un collegamento solo sul desktop non è altrettanto efficace come includerlo nella schermata Start.

![Diagramma che mostra la griglia con un riquadro dell'applicazione, le dimensioni e "Segoe U I SemiLight" per indicare il tipo di carattere usato.](images/tiles-desktop-2.png)

No: non specificare più collegamenti alla stessa app. Ad esempio, non sono disponibili due tasti di scelta rapida che avviano un'app in due modalità diverse, ad esempio una per Windows Internet Explorer e una per Internet Explorer senza componenti aggiuntivi.

DO: ridurre il numero di riquadri aggiunti come parte dell'installazione. Si consiglia di esporre altri punti di ingresso alle app estranee. Ad esempio, invece di includere un'app impostazioni separate con un'app console, accedere alle impostazioni tramite una funzionalità nell'app console.

NON: non inserire i collegamenti agli elementi seguenti nella schermata Start:

-   Disinstallazione. Gli utenti possono accedere al programma di disinstallazione tramite l'elemento programmi nel pannello di controllo.
-   File della guida. Includere gli argomenti della Guida direttamente nell'app.
-   Impostazioni e opzioni dell'app. Includere l'interfaccia utente per configurare le impostazioni per un'app all'interno dell'app o creare un elemento del pannello di controllo.
-   Siti Web. Fornire i collegamenti appropriati a informazioni quali i siti di supporto tecnico e di assistenza direttamente nell'app.
-   Procedure guidate. Le procedure guidate e altre attività di configurazione una sola volta devono essere avviate dall'interno dell'app.

NON: non creare collegamenti a funzionalità o funzionalità che possono essere avviate dall'interno dell'app stessa. Ad esempio, le impostazioni della lingua possono essere configurate da qualsiasi app Microsoft Office, quindi non è necessario anche avere un punto di ingresso Impostazioni lingua separato nella schermata Start.

NON: non creare collegamenti ad elementi che non sono file eseguibili. I tasti di scelta rapida che non eseguono il mapping a file eseguibili, ad esempio i collegamenti che avviano siti Web o file della guida, vengono esclusi dalla schermata Start.

DO: se si installa una suite di app anziché una singola app, aggiungere un collegamento per ogni app della suite. Come indicato in precedenza, evitare di creare collegamenti a funzionalità secondarie, ad esempio informazioni della guida, utilità e impostazioni. Questa funzionalità deve essere inclusa nelle app rilevanti del gruppo.

DO: creare una cartella del prodotto a livello singolo per i gruppi che contengono tre o più riquadri. Nella visualizzazione App della schermata Start, accessibile dall'accesso alla ricerca, le applicazioni vengono raggruppate in base alla cartella di primo livello. Scegliere un nome di cartella descrittivo ma conciso; sono consigliate tre parole o meno. Tenere presente che, mentre la visualizzazione App raggruppa i riquadri e Mostra il nome della cartella, questo nome non è visibile quando un riquadro viene aggiunto alla schermata Start, quindi rendere i nomi dei riquadri sufficientemente descrittivi.

NON creare una cartella del prodotto se il gruppo contiene un solo collegamento. Inserire il collegamento nella cartella di avvio di primo livello.

DO: quando si installa una suite di più di tre app, valutare se una di queste app è per uso secondario, più irregolare e non deve essere bloccata alla schermata Start. In tal caso, è possibile che i riquadri vengano rimossi completamente, in base alle indicazioni precedenti, e che vengano avviati dall'interno di un'app primaria. Se non è possibile rimuovere i riquadri, è consigliabile rimuoverli dalla schermata Start. In questo modo, i tasti di scelta rapida vengono comunque visualizzati nella visualizzazione **tutte le app** , ma non ingombrano la schermata iniziale dell'utente.

Per creare un collegamento all'app senza aggiungerlo alla schermata Start, impostare la proprietà seguente nel collegamento: System. AppUserModel. StartPinOption = 1. Il nome simbolico di 1 è APPUSERMODEL \_ STARTPINOPTION \_ NOPINONINSTALL.

In questo modo si impedisce che il collegamento venga visualizzato nella schermata Start, ma può comunque essere visualizzato nella visualizzazione **tutte le app** e nei risultati della ricerca. Solo l'utente può Rimuovi i collegamenti esistenti, quindi è necessario impostare questa proprietà durante l'installazione o immediatamente dopo aver posizionato l'app su disco.

NON: non creare un riquadro per un host o un runtime per le applicazioni, ad esempio Silverlight o Java. Fornire un punto di ingresso per disinstallare il Framework in Installazione applicazioni e fornire qualsiasi punto di ingresso delle impostazioni nel pannello di controllo.

 

 



