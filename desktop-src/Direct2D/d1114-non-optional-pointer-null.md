---
title: D1114 Puntatore non facoltativo NULL
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: Il parametro per interface::method non è facoltativo. È stato passato un puntatore NULL. Ciò causerà l'arresto anomalo di Direct2D.
keywords:
- D1114 Puntatore non facoltativo NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fa5213eabfb4b22b9a37927495f5058cbfeb0b86b0f1f8b8f3a4ba1a2a2bdbb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666210"
---
# <a name="d1114-non-optional-pointer-null"></a>D1114: Puntatore non facoltativo NULL

Il parametro \[ *del parametro* \] per il *metodo* dell'interfaccia :: non è facoltativo. È stato passato un puntatore **NULL.** Ciò causerà l'arresto anomalo di Direct2D.

### <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*Parametro*
</dt> <dd>

Nome del parametro che contiene il **puntatore NULL.**

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaccia*
</dt> <dd>

Nome dell'interfaccia a cui appartiene *il* metodo.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*Metodo*
</dt> <dd>

Nome del metodo che ha ricevuto il parametro non valido.

</dd> </dl> 




 

### <a name="examples"></a>Esempio

L'esempio seguente mostra che il [**metodo FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) riceve un puntatore NULL per il parametro *geometry* non facoltativo.


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



In questo esempio viene generato il messaggio di debug seguente:

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a>Possibili cause

È stato passato un puntatore NULL per un parametro non facoltativo.

## <a name="fixes"></a>Correzioni

Assicurarsi che un parametro non facoltativo non abbia un puntatore NULL.

 

 
