---
title: D1114 puntatore non facoltativo NULL
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: "Il parametro per Interface:: Method non è facoltativo. È stato passato un puntatore NULL. Questo provocherà l'arresto anomalo di Direct2D."
keywords:
- D1114 non facoltativo puntatore NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "106334159"
---
# <a name="d1114-non-optional-pointer-null"></a>D1114: puntatore NULL non facoltativo

Il parametro \[ *Parameter* \] per *Interface*::*Method* non è facoltativo. È stato passato un puntatore **null** . Questo provocherà l'arresto anomalo di Direct2D.

### <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*parametro*
</dt> <dd>

Nome del parametro che contiene il puntatore **null** .

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interfaccia*
</dt> <dd>

Nome dell'interfaccia a cui appartiene il *Metodo* .

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*Metodo*
</dt> <dd>

Nome del metodo che ha ricevuto il parametro non valido.

</dd> </dl> 




 

### <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato che il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) riceve un puntatore null per il parametro *Geometry* non facoltativo.


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



Questo esempio produce il seguente messaggio di debug:

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a>Possibili cause

È stato passato un puntatore NULL per un parametro non facoltativo.

## <a name="fixes"></a>Correzioni

Verificare che un parametro non facoltativo non disponga di un puntatore NULL.

 

 
