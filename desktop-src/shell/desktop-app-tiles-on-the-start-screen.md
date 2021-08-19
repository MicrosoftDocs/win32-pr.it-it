---
description: Di seguito vengono fornite informazioni sulle scelte da considerare per personalizzare i riquadri delle app desktop per Windows 8 tra cui come progettare riquadri di app desktop per il nuovo schermata Start e come scegliere i punti di ingresso da visualizzare nel schermata Start.
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: Riquadri dell'app desktop nella schermata Start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ed35bd5c8405301e872ef54774914d625e1fc06c6a9fc3c26965e130301eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861222"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a>Riquadri dell'app desktop nella schermata Start

Di seguito vengono fornite informazioni sulle scelte da considerare per personalizzare i riquadri delle app desktop per Windows 8 tra cui come progettare riquadri di app desktop per il nuovo schermata Start e come scegliere i punti di ingresso da visualizzare nel schermata Start.

## <a name="design-your-tile-for-the-start-screen"></a>Progettare il riquadro per il schermata Start

È possibile personalizzare due aspetti dei riquadri dell'app desktop: il nome dell'app e l'icona. Il colore di sfondo deriva dal colore di sfondo scelto dall'utente e non è personalizzabile a livello di codice.

![Linee guida per la progettazione del riquadro dell'app.](images/tiles-desktop-1.png)

DO: evitare il troncamento del nome dell'applicazione. I riquadri del desktop aggiunti al schermata Start possono contenere fino a due righe di testo per riga o una decina di caratteri (anche se dipende dalla lingua dell'interfaccia utente), quindi provare a mantenere il nome dell'applicazione sufficientemente breve da evitare il troncamento.

DO: specificare le icone per i quattro valori di scala schermata Start supportati per garantire che le icone siano nitide in tutti i fattori di forma.



| Scalabilità | Dimensioni del riquadro (in pixel) | Dimensioni dell'icona usate (in pixel) |
|-------|-----------------------|----------------------------|
| 80%   | 120 x 120             | 48 x 48                    |
| 100%  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

DO: Adottare i principi di progettazione Microsoft. Il nuovo aspetto delle icone è semplice, quindi se si vuole simulare le icone dell'app di Windows Store per l'app desktop, è consigliabile rimuovere le ombreggiature e così via.

DON'T: non evitare l'uso del colore. Anche Windows icone delle app dello Store sono talvolta monocromatiche, è consigliabile usare le icone a colori per le app desktop. Ciò consente di distinguere le applicazioni desktop sulla barra delle applicazioni e da altri riquadri dell'app desktop nel schermata Start perché il colore di sfondo dei riquadri desktop non può essere personalizzato. Prendere in considerazione l'uso di colori più saturati.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Decidere i punti di ingresso da includere nel schermata Start

DO: Aggiungere un collegamento per ogni app nel schermata Start quando l'app viene installata. Ciò garantisce che gli utenti possano avviare l'app direttamente dal schermata Start o tramite la ricerca. Se non si include un collegamento nel schermata Start, l'app diventa difficile da avviare. In particolare, non aggiungere un collegamento solo sul desktop. Gli utenti visualizzano schermata Start al primo accesso e quindi l'inserimento di un collegamento solo sul desktop non è efficace quanto includerlo nel schermata Start.

![Diagramma che mostra una griglia con un riquadro dell'applicazione, dimensioni e "Segoe U I Semilight" per indicare il tipo di carattere usato.](images/tiles-desktop-2.png)

DON'T: non fornire più collegamenti alla stessa app. Ad esempio, non sono disponibili due tasti di scelta rapida che avviano un'app in due modalità diverse, ad esempio una per Windows Internet Explorer e una per Internet Explorer senza componenti aggiuntivi.

DO: ridurre al minimo il numero di riquadri aggiunti durante l'installazione. Valutare la possibilità di esporre altri punti di ingresso alle app estranee. Ad esempio, invece di includere un'app Impostazioni separata con un'app console, accedere alle impostazioni tramite una funzionalità nell'app console.

DON'T: Non inserire collegamenti agli elementi seguenti nel schermata Start:

-   Disinstallazione. Gli utenti possono accedere ai programmi di disinstallazione tramite l'elemento Programmi nella Pannello di controllo.
-   File della Guida. Includere argomenti della Guida direttamente nell'app.
-   Impostazioni e opzioni dell'app. Includere l'interfaccia utente per configurare le impostazioni per un'app all'interno dell'app o creare un Pannello di controllo elemento.
-   Siti Web. Fornire i collegamenti appropriati a informazioni come la Guida e i siti di supporto tecnico direttamente nell'app.
-   Procedure guidate. Le procedure guidate e altre attività di configurazione una sola volta devono essere avviate dall'interno dell'app.

DON'T: non creare collegamenti a funzionalità o funzionalità che possono essere avviate dall'interno dell'app stessa. Ad esempio, language Impostazioni può essere configurato da qualsiasi app Microsoft Office, pertanto non è necessario avere un punto di ingresso language Impostazioni separato nel schermata Start.

DON'T: non creare collegamenti a elementi che non sono file eseguibili. I collegamenti che non sono mappati a file eseguibili, ad esempio collegamenti che avviano siti Web o file della Guida, vengono filtrati schermata Start.

DO: se si installa una suite di app anziché una singola app, aggiungere un collegamento per ogni app nella suite. Come accennato in precedenza, evitare di creare collegamenti a funzionalità secondarie come informazioni della Guida, utilità e impostazioni. Tale funzionalità deve essere inclusa nelle app pertinenti della suite.

DO: Creare una cartella di prodotti a livello singolo per le suite che contengono tre o più riquadri. Nella visualizzazione App del schermata Start, accessibile dall'accesso alla ricerca, le applicazioni vengono raggruppate in base alla cartella di primo livello. Scegliere un nome di cartella descrittivo ma conciso. Sono consigliate tre parole o meno. Tenere presente che mentre la visualizzazione App raggruppa i riquadri e mostra il nome della cartella, questo nome non è visibile quando un riquadro viene aggiunto al schermata Start, quindi rendere sufficientemente descrittivi i nomi dei riquadri.

DON'T: non creare una cartella del prodotto se la suite contiene un solo collegamento. Posizionare il collegamento nella cartella Start di primo livello.

DO: quando si installa una suite di più di tre app, valutare se una di queste app è per un uso secondario e più irregolare e non deve essere aggiunta al schermata Start. In tal caso, è possibile rimuovere completamente questi riquadri, in base alle indicazioni riportate in precedenza, e avviarsi dall'interno di un'app primaria. Se non è possibile rimuovere i riquadri, è consigliabile rimuoverli dal schermata Start. In questo modo, i  tasti di scelta rapida vengono comunque visualizzati nella visualizzazione Tutte le app, ma non ingombrano le schermata Start.

Per creare un collegamento all'app senza aggiungerlo al schermata Start, impostare la proprietà seguente nel collegamento: System.AppUserModel.StartPinOption = 1. Il nome simbolico per 1 è APPUSERMODEL \_ STARTPINOPTION \_ NOPINONINSTALL.

In questo modo il collegamento non viene visualizzato nel schermata Start, ma può comunque essere visualizzato nella visualizzazione Tutte le **app** e nei risultati della ricerca. Solo l'utente può rimuovere i collegamenti esistenti, pertanto è necessario impostare questa proprietà durante l'installazione o immediatamente dopo aver posizionato l'app su disco.

DON'T: non creare un riquadro per un host o un runtime per applicazioni, ad esempio Silverlight o Java. Fornire un punto di ingresso per disinstallare il framework in Installazione applicazioni e fornire qualsiasi punto di ingresso delle impostazioni Pannello di controllo.

 

 



