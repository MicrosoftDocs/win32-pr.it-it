---
description: Tempo in servizi di modifica DirectShow
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: Tempo in servizi di modifica DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421831742a2805f58d61c2258dad89d339131f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319546"
---
# <a name="time-in-directshow-editing-services"></a>Tempo in servizi di modifica DirectShow

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Per modificare il video, è necessario usare alcuni concetti importanti relativi alla tempistica. Ad esempio:

-   Ogni clip ha una durata.
-   Le clip, le transizioni e gli effetti vengono visualizzati in determinati orari in un progetto.
-   Il video presenta una frequenza di fotogrammi, espressa in frame al secondo (fps).

I [servizi di modifica DirectShow](directshow-editing-services.md) (des) forniscono diversi metodi che consentono di impostare o recuperare orari e frequenze dei fotogrammi. Il significato di questi valori dipende dal contesto.

**Valori temporali**

Quando un parametro esprime un'ora, sono possibili tre significati distinti:

-   *Time Timeline*: tempo relativo all'inizio della sequenza temporale. Ad esempio, una clip potrebbe iniziare 2 secondi nella sequenza temporale o una transizione potrebbe verificarsi 15 secondi nella sequenza temporale. La sequenza temporale determina il progetto di cui è stato eseguito il rendering finale, quindi è possibile considerare anche il tempo della sequenza temporale come "tempo progetto".
-   *Tempo del supporto*: punto in un file di origine relativo all'inizio del file, come raggiunto durante la riproduzione normale. Se, ad esempio, si dispone di un file video di 10 secondi, il punto a metà del file si verifica a 5 secondi, espresso come ora del supporto.
-   *Ora padre*: tempo relativo a un oggetto nella sequenza temporale. Se, ad esempio, un oggetto inizia a 8 secondi nella sequenza temporale e contiene un altro oggetto che inizia a 10 secondi nella sequenza temporale, l'oggetto figlio inizia a 2 secondi rispetto all'elemento padre. Tutte le tracce virtuali iniziano al momento zero rispetto alla sequenza temporale. Quindi, per qualsiasi oggetto in una traccia virtuale, l'ora padre è uguale all'ora della sequenza temporale.

Il tempo di supporto si applica solo agli oggetti di origine. Ogni oggetto di origine ha un'ora di inizio e un'ora di arresto del supporto. Si supponga, ad esempio, di avere un clip video di 10 secondi e di voler usare solo 5 secondi dal centro della clip, tagliando i primi 2 secondi e gli ultimi 3 secondi dalla clip. Se si vuole che il clip venga visualizzato 20 secondi nel progetto (e presupponendo una frequenza di riproduzione normale), specificare le ore di inizio e di fine seguenti.

-   Inizio supporto: 2 secondi
-   Arresto supporto: 7 secondi
-   Inizio sequenza temporale: 20 secondi
-   Arresto sequenza temporale: 25 secondi

    ![inserimento di una clip di origine in una sequenza temporale](images/des-time1.png)

**Frequenza fotogrammi**

La frequenza dei fotogrammi è la "velocità" di un flusso multimediale, misurata in fotogrammi al secondo. Come per i valori temporali, il significato di una frequenza dei fotogrammi dipende dal contesto:

-   **Frequenza fotogrammi di output:** Frequenza dei fotogrammi del progetto di cui è stato eseguito il rendering finale, definito dal gruppo. Quando si esegue il rendering del progetto, ogni gruppo diventa un flusso multimediale separato con la relativa frequenza dei fotogrammi.
-   **Frequenza fotogrammi di origine:** Frequenza dei fotogrammi in cui è stato originariamente creato il file di origine. La frequenza dei fotogrammi creata non deve corrispondere alla frequenza dei fotogrammi di output del gruppo. DES effettuerà automaticamente il campionamento o Downsample il file in base alle esigenze. Per la maggior parte dei formati multimediali, DES può determinare la frequenza dei fotogrammi esaminando il formato. Una sequenza DIB è un'eccezione. è necessario specificare la frequenza dei fotogrammi di una sequenza DIB. Per ulteriori informazioni, vedere [utilizzo delle origini](working-with-sources.md).

**Velocità di riproduzione:** Velocità apparente di una clip di origine quando viene visualizzata nel progetto. Ad esempio, 10 secondi di video possono essere inseriti in 5 secondi nella sequenza temporale. Di conseguenza, la velocità della clip aumenta di un fattore pari a 2, come illustrato nella figura seguente.

![esecuzione più veloce di un'origine](images/des-time2.png)

Con un'origine audio, anche il pitch viene spostato. La formula seguente determina la velocità di riproduzione di una clip di origine:

-   Velocità di riproduzione = (Media Stop-avvio supporto)/(arresto sequenza temporale-Avvio sequenza temporale)

Si noti che ognuno di questi tre tassi è indipendente dagli altri:

-   È possibile velocizzare o rallentare un ritaglio regolando i tempi dei supporti; Questa operazione non influisce sulla frequenza dei fotogrammi dell'output finale.
-   È possibile aumentare o ridurre la frequenza dei fotogrammi di output senza influenzare la velocità di riproduzione di un file.
-   È possibile combinare, all'interno dello stesso gruppo, i file di origine con diverse frequenze di frame create e DES esegue il campionamento o il downsample di ogni clip in modo che corrisponda alla frequenza dei fotogrammi del gruppo.

Quando si esegue il rendering di un progetto, tutte le volte vengono arrotondate al limite del frame più vicino, come determinato dalla frequenza dei fotogrammi del gruppo. Si supponga, ad esempio, che un gruppo di video abbia una frequenza di fotogrammi pari a 30 fps. Ogni frame è approssimativamente di 33 millisecondi (MS). Si supponga di aggiungere una clip di origine di 1,68 secondi alla sequenza temporale, a partire dal momento zero. L'origine non termina esattamente su un limite di frame, quindi DES arrotonda il tempo di arresto a 1,6666 secondi (50 frame). Se si cerca di 1,68 secondi nel progetto di cui è stato eseguito il rendering, si procederà alla fine del 51 ° frame.

Tuttavia, DES non sovrascrive l'ora di arresto dell'origine. In seguito è possibile modificare la frequenza dei fotogrammi del gruppo o spostare l'origine in un nuovo punto della sequenza temporale in cui viene arrotondato in modo diverso. Quindi, DES conserva l'ora di arresto originale e arrotonda solo quando necessario. Per ulteriori informazioni, vedere [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con i servizi di modifica DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



