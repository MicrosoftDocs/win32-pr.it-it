---
description: La proprietà DVDDirectory imposta o recupera la directory corrente del volume DVD corrente.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Proprietà DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876573"
---
# <a name="dvddirectory-property"></a>Proprietà DVDDirectory

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDDirectory` proprietà imposta o recupera la directory corrente del volume DVD corrente.

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore stringa che indica il percorso della directory radice DVD.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito. Utilizzare questo metodo per impostare il percorso radice quando è presente più di un'unità DVD in un sistema. Quando nel sistema è presente una sola unità e la lettera di unità è superiore a "C", l'oggetto MSWebDVD lo trova automaticamente. Per un disco DVD-Video standard, il percorso radice deve includere la directory video di Servizi terminal \_ :


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



Alcuni volumi DVD possono avere un video in una directory denominata qualcosa di diverso da "video \_ TS". L'idea generale è che un "volume DVD" aggiuntivo (il set di. IFO. VOB, e. I file BUP normalmente archiviati nella \_ directory di Servizi terminal video possono essere inseriti in una sottodirectory del disco. Cambiando la radice in modo che punti a questa directory, MSWebDVD funzionerà su questo volume DVD separato. Sarà disponibile un nuovo set di menu, titoli e così via, indipendentemente dai titoli nella radice del VIDEO \_ TS, che non sarà più accessibile. Tali directory sono denominate "directory nascoste". Nell'esempio seguente viene illustrato come impostare una directory nascosta come radice, dove "hidden" è un segnaposto per qualsiasi nome assegnato alla directory dagli autori del disco.


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



