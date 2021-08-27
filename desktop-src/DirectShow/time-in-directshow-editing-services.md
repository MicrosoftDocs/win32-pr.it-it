---
description: Tempo di DirectShow servizi di modifica
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: Tempo di DirectShow servizi di modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc99ff2391ea7975daed7b4152e869741f9990561417131942c4d86e904fca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083623"
---
# <a name="time-in-directshow-editing-services"></a>Tempo di DirectShow servizi di modifica

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Per modificare i video, è necessario usare alcuni importanti concetti di temporizzazione. Esempio:

-   Ogni clip ha una durata.
-   Le clip, le transizioni e gli effetti vengono visualizzati in determinati momenti in un progetto.
-   Il video ha una frequenza di fotogrammi espressa in fotogrammi al secondo (fps).

[DirectShow Editing Services](directshow-editing-services.md) (DES) fornisce vari metodi che impostano o recuperano orari e frequenze fotogrammi. Il significato di questi valori dipende dal contesto.

**Valori di ora**

Quando un parametro esprime un tempo, sono possibili tre significati distinti:

-   *Tempo sequenza temporale:* tempo relativo all'inizio della sequenza temporale. Ad esempio, un clip potrebbe iniziare 2 secondi nella sequenza temporale o potrebbe verificarsi una transizione di 15 secondi nella sequenza temporale. La sequenza temporale determina il progetto di cui è stato eseguito il rendering finale, quindi è anche possibile pensare all'ora della sequenza temporale come "ora del progetto".
-   *Tempo multimediale:* punto in un file di origine rispetto all'inizio del file, raggiunto durante la riproduzione normale. Ad esempio, se si dispone di un file video di 10 secondi, il punto a metà del file si verifica a 5 secondi, espresso come tempo multimediale.
-   *Ora padre:* tempo relativo a un oggetto nella sequenza temporale. Ad esempio, se un oggetto inizia a 8 secondi sulla sequenza temporale e contiene un altro oggetto che inizia a 10 secondi sulla sequenza temporale, l'oggetto figlio inizia a 2 secondi rispetto all'oggetto padre. Le tracce virtuali iniziano tutte con il tempo zero, rispetto alla sequenza temporale. Pertanto, per qualsiasi oggetto in una traccia virtuale, il tempo padre è uguale al tempo della sequenza temporale.

Il tempo multimediale si applica solo agli oggetti di origine. Ogni oggetto di origine ha un'ora di inizio del supporto e un'ora di arresto del supporto. Si supponga, ad esempio, di avere un clip video di 10 secondi e di voler usare solo 5 secondi dalla metà del clip, tagliando i primi 2 secondi e gli ultimi 3 secondi dal clip. Se si vuole che il clip venga visualizzato 20 secondi nel progetto (presupponendo una velocità di riproduzione normale), è necessario specificare i tempi di avvio e arresto seguenti.

-   Avvio del supporto: 2 secondi
-   Arresto del supporto: 7 secondi
-   Inizio sequenza temporale: 20 secondi
-   Interruzione della sequenza temporale: 25 secondi

    ![inserimento di un clip di origine in una sequenza temporale](images/des-time1.png)

**Frequenze fotogrammi**

Frequenza fotogrammi è la "velocità" di un flusso multimediale, misurata in fotogrammi al secondo. Come per i valori di tempo, il significato di una frequenza fotogrammi dipende dal contesto:

-   **Frequenza fotogrammi di output:** Frequenza dei fotogrammi del progetto di cui è stato eseguito il rendering finale, definito dal gruppo. Quando si esegue il rendering del progetto, ogni gruppo diventa un flusso multimediale separato con la propria frequenza di fotogrammi.
-   **Frequenza fotogrammi di origine:** Frequenza dei fotogrammi in cui è stato originariamente creato il file di origine. La frequenza dei fotogrammi creati non deve corrispondere alla frequenza dei fotogrammi di output del gruppo. DES esemperà automaticamente il campionamento o il downsample del file in base alle esigenze. Per la maggior parte dei formati multimediali, DES può determinare la frequenza dei fotogrammi esaminando il formato. Una sequenza DIB è un'eccezione. è necessario specificare la frequenza dei fotogrammi di una sequenza DIB. Per altre informazioni, vedere [Uso delle origini.](working-with-sources.md)

**Velocità di riproduzione:** Velocità apparente di un clip di origine quando viene visualizzato nel progetto. Ad esempio, 10 secondi di video possono essere contenuti in 5 secondi nella sequenza temporale. Di conseguenza, la velocità della clip aumenta di un fattore di 2, come illustrato nel diagramma seguente.

![rendere più veloce una riproduzione di origine](images/des-time2.png)

Con un'origine audio, anche l'intonazione cambia. La formula seguente determina la velocità di riproduzione di un clip di origine:

-   Velocità di riproduzione = (Arresto multimediale - Avvio multimediale) / (Arresto sequenza temporale - Avvio sequenza temporale)

Si noti che ognuna di queste tre tariffe è indipendente dalle altre:

-   È possibile accelerare o rallentare un clip regolando i tempi dei supporti; ciò non influisce sulla frequenza dei fotogrammi dell'output finale.
-   È possibile aumentare o ridurre la frequenza dei fotogrammi di output senza influire sulla velocità di riproduzione di un file.
-   È possibile combinare, all'interno dello stesso gruppo, file di origine con frequenze di fotogrammi creati diverse e DES esempere o sottocampionare ogni clip in modo che corrisponda alla frequenza dei fotogrammi del gruppo.

Quando si esegue il rendering di un progetto, tutte le volte vengono arrotondate al limite del frame più vicino, come determinato dalla frequenza fotogrammi del gruppo. Si supponga, ad esempio, che un gruppo di video abbia una frequenza fotogrammi di 30 fps. Ogni fotogramma è di circa 33 millisecondi (ms). Si supponga di aggiungere un clip di origine di 1,68 secondi alla sequenza temporale, a partire dal momento zero. L'origine non termina esattamente su un limite di frame, quindi DES arrotonda il tempo di arresto a 1,6666 secondi (50 fotogrammi). Se si cerca di 1,68 secondi nel progetto sottoposto a rendering, si cercherà effettivamente oltre la fine dell'origine, fino al 51° frame.

Des non sovrascrive tuttavia il tempo di arresto dell'origine. In un secondo momento è possibile modificare la frequenza fotogrammi del gruppo o spostare l'origine in un nuovo punto della sequenza temporale in cui viene arrotondato in modo diverso. Des mantiene pertanto il tempo di arresto originale e arrotonda solo quando necessario. Per altre informazioni, vedere [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con i DirectShow di modifica](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



