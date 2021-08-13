---
description: Dichiarare una classe C++ che eredita la classe di base scelta nell'ambito della scrittura di un filtro di trasformazione.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Passaggio 2. Dichiarare la classe Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3e814802a67185f320345dea2f397188999ecafb9596b9b368a4b6eff8e240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652197"
---
# <a name="step-2-declare-the-filter-class"></a>Passaggio 2. Dichiarare la classe Filter

Questo è il passaggio 2 dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)

Per iniziare, dichiarare una classe C++ che eredita la classe di base:


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



A ognuna delle classi di filtro sono associate classi pin. A seconda delle esigenze specifiche del filtro, potrebbe essere necessario eseguire l'override delle classi pin. Nel caso di **CTransformFilter,** i segnaposto delegano la maggior parte del lavoro al filtro, quindi probabilmente non è necessario eseguire l'override dei pin.

È necessario generare un CLSID univoco per il filtro. È possibile usare l'utilità Guidgen o Uuidgen. non copiare mai un GUID esistente. Esistono diversi modi per dichiarare un CLSID. Nell'esempio seguente viene utilizzata la macro **DEFINE \_ GUID:**


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



Scrivere quindi un metodo costruttore per il filtro:


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



Si noti che uno dei parametri per il [**costruttore CTransformFilter**](ctransformfilter-ctransformfilter.md) è il CLSID definito in precedenza.

Passaggio [successivo: Passaggio 3. Supporto della negoziazione del tipo di supporto](step-3--support-media-type-negotiation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



