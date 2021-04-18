---
description: Aggiunta di un'origine
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Aggiunta di un'origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304270"
---
# <a name="adding-a-source"></a>Aggiunta di un'origine

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Creare un oggetto di origine nello stesso modo in cui si creano altri oggetti della sequenza temporale. Prima di inserirlo nella sequenza temporale, tuttavia, è necessario specificare almeno le proprietà seguenti nell'origine.

-   Ora di inizio e di fine rispetto alla sequenza temporale. Chiamare il metodo [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) .
-   File multimediale da utilizzare come origine. Chiamare il metodo [**IAMTimelineSrc:: Semedianame**](iamtimelinesrc-setmedianame.md) con una stringa di caratteri wide che rappresenta il nome del file.
-   L'ora di inizio e di fine del supporto, che sono relative al file originale. Chiamare il metodo [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . Per altre informazioni sui tempi dei supporti, vedere [Time in DirectShow editing Services](time-in-directshow-editing-services.md).

Nell'esempio seguente il clip di origine inizia quattro secondi nel file. La durata del supporto è di 10 secondi, il doppio della durata della sequenza temporale, che indica che l'origine verrà riprodotto alla velocità di due volte normale. Le unità di costante sono definite come 10 milioni (10 ^ 7) ed è uguale a un secondo.


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> Attualmente, DES non può eseguire contemporaneamente il rendering di più di 75 origini compresse con codec di Gestione compressione video (VCM). Inoltre, se il progetto contiene più di 75 origini di questo tipo, è necessario utilizzare la riconnessione dinamica oppure il programma DES non può visualizzare in anteprima il progetto. Per ulteriori informazioni, vedere [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

 

Per ulteriori informazioni sulle origini, vedere [utilizzo delle origini](working-with-sources.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 



