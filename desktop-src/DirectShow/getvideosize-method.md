---
description: Il metodo GetVideoSize recupera le dimensioni video native.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Metodo GetVideoSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304386"
---
# <a name="getvideosize-method"></a>Metodo GetVideoSize

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetVideoSize` metodo recupera le dimensioni video native.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Valore restituito

Restituisce un oggetto [DVDRect](dvdrect-object.md) che contiene quattro proprietà di lettura/scrittura: (in alto a sinistra) x; (in alto a sinistra) y, larghezza e altezza. Le proprietà **x** e **y** sono impostate su zero e le altre due proprietà riflettono la larghezza e l'altezza del rettangolo video come creato sul disco.

 

 



