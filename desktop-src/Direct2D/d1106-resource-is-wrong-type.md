---
title: Il tipo della risorsa D1106 non è corretto
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: La risorsa specificata non è di un tipo previsto.
keywords:
- La risorsa D1106 non è di tipo Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "106334162"
---
# <a name="d1106-resource-is-wrong-type"></a>D1106: la risorsa è di tipo errato

La risorsa della risorsa specificata \[  \] non è di un tipo previsto.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*risorse*
</dt> <dd>

Indirizzo della risorsa.

</dd> </dl> 




 

## <a name="possible-causes"></a>Possibili cause

Un'interfaccia è stata cast e usata in modo errato come parametro per un metodo o una funzione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene passato un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) quando è previsto un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



Questo esempio produce il seguente messaggio di debug:

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a>Correzioni

Usare il tipo richiesto dal metodo.

 

 
