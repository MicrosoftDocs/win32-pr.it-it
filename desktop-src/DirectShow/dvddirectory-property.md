---
description: La proprietà DVDDirectory imposta o recupera la directory corrente del volume DVD corrente.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Proprietà DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2431d9255aa743698baeb9c4b8427ffa9bf5220a60182ac08c246e11f20bcec8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749101"
---
# <a name="dvddirectory-property"></a>Proprietà DVDDirectory

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDDirectory` proprietà imposta o recupera la directory corrente del volume DVD corrente.

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore stringa che indica il percorso della directory radice del DVD.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura senza alcun valore predefinito. Usare questo metodo per impostare il percorso radice quando in un sistema sono presenti più unità DVD. Quando nel sistema è presente una sola unità e la lettera di unità è superiore a "C", l'oggetto MSWebDVD la trova automaticamente. Per un disco DVD-Video standard, il percorso radice deve includere la \_ directory video ts:


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



Alcuni volumi DVD possono contenere il proprio video in una directory con un nome diverso da "video \_ ts". L'idea generale è che un "volume DVD" aggiuntivo (il set di . Ifo. VOB e . I file BUP che normalmente vengono archiviati nella directory VIDEO TS) possono essere inseriti \_ in una sottodirectory sul disco. Modificando la radice in modo che punti a questa directory, MSWebDVD funzionerà su questo volume DVD separato. Sarà disponibile un nuovo set di menu, titoli e così via, indipendentemente dai titoli nella radice di VIDEO TS, che non \_ saranno più accessibili. Tali directory sono denominate "directory nascoste". L'esempio seguente illustra come impostare una directory nascosta come radice, dove "hidden" è un segnaposto per qualsiasi nome assegnato dagli autori del disco alla directory.


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



