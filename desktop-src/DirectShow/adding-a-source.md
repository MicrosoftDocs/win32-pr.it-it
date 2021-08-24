---
description: Aggiunta di un'origine
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Aggiunta di un'origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab2440ff50bbb4a3a610f9341405538a88dc6bf16ce2153a327f3b4578f3aec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690531"
---
# <a name="adding-a-source"></a>Aggiunta di un'origine

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Creare un oggetto di origine nello stesso modo in cui si creano altri oggetti sequenza temporale. Prima di inserirlo nella sequenza temporale, tuttavia, è necessario specificare almeno le proprietà seguenti nell'origine.

-   Ora di inizio e di arresto, rispetto alla sequenza temporale. Chiamare il [**metodo IAMTimelineObj::SetStartStop.**](iamtimelineobj-setstartstop.md)
-   File multimediale da usare come origine. Chiamare il [**metodo IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) con una stringa di caratteri wide che rappresenta il nome del file.
-   Ora di inizio e di arresto dei supporti, relativi al file originale. Chiamare il [**metodo IAMTimelineSrc::SetMediaTimes.**](iamtimelinesrc-setmediatimes.md) Per altre informazioni sui tempi dei file multimediali, vedere [Time in DirectShow Editing Services.](time-in-directshow-editing-services.md)

Nell'esempio seguente il clip di origine inizia quattro secondi nel file. La durata del contenuto multimediale è di 10 secondi, il doppio della durata della sequenza temporale, vale a dire che l'origine verrà riprodotta a una velocità doppia rispetto alla normale. La costante UNITS è definita come 100000000 (10^7) ed è uguale a un secondo.


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> Attualmente, DES non può eseguire il rendering simultaneo di più di 75 origini compresse con codec VCM (Video Compression Manager). Inoltre, se il progetto nel suo complesso contiene più di 75 origini di questo tipo, è necessario usare la riconnessione dinamica o DES non può visualizzare in anteprima il progetto. Per altre informazioni, vedere [**IRenderEngine::SetDynamicReconnectLevel.**](irenderengine-setdynamicreconnectlevel.md)

 

Per altre informazioni sulle origini, vedere [Uso delle origini.](working-with-sources.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costruzione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 



