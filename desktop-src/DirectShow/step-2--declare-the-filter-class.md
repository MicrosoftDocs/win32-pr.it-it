---
description: 'Passaggio 2:'
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: 'Passaggio 2: Dichiarare la classe filter'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ddfe28b7f31238089c331b319621787aef49f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315938"
---
# <a name="step-2-declare-the-filter-class"></a>Passaggio 2: Dichiarare la classe filter

Questo è il passaggio 2 dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).

Iniziare dichiarando una classe C++ che eredita la classe di base:


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



A ognuna delle classi di filtro sono associate classi pin. A seconda delle esigenze specifiche del filtro, potrebbe essere necessario eseguire l'override delle classi pin. Nel caso di **CTransformFilter**, i pin delegano la maggior parte del lavoro al filtro, quindi probabilmente non è necessario eseguire l'override dei pin.

È necessario generare un CLSID univoco per il filtro. È possibile utilizzare l'utilità Guidgen o uuidgen. non copiare mai un GUID esistente. Esistono diversi modi per dichiarare un CLSID. Nell'esempio seguente viene usata la macro **Definisci \_ GUID** :


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



Successivamente, scrivere un metodo del costruttore per il filtro:


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



Si noti che uno dei parametri del costruttore [**CTransformFilter**](ctransformfilter-ctransformfilter.md) è il CLSID definito in precedenza.

Successivo: [passaggio 3. Supporto della negoziazione del tipo](step-3--support-media-type-negotiation.md)di supporto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



