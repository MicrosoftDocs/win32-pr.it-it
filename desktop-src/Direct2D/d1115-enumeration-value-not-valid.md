---
title: Valore di enumerazione D1115 non valido
description: Valore di enumerazione D1115 non valido
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- Valore di enumerazione D1115 non valido direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11800acaae350b5289b339738448300c91db32a16c0d3f3d9224f08b6079fba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758121"
---
# <a name="d1115-enumeration-value-not-valid"></a>D1115: Valore di enumerazione non valido

Il parametro \[ *del parametro* \] con valore value \[ *per* \] il *metodo* dell'interfaccia :: non è un valore di enumerazione valido.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*Parametro*
</dt> <dd>

Nome del parametro che ha ricevuto il tipo imprevisto.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valore*
</dt> <dd>

Valore di enumerazione non valido.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaccia*
</dt> <dd>

Nome dell'interfaccia a cui appartiene *il* metodo.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*Metodo*
</dt> <dd>

Nome del metodo che ha ricevuto il valore di enumerazione non valido.

</dd> </dl> 




 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene specificato un valore di enumerazione [**D2D1 \_ RENDER TARGET \_ \_ TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) pari a 30, che non rientra nell'intervallo previsto.


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



In questo esempio viene generato il messaggio di debug seguente:

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a>Possibili cause

Un parametro ha usato un valore di enumerazione non valido.

## <a name="fixes"></a>Correzioni

Usare un valore di enumerazione valido.

> [!Note]  
> Il livello di debug controlla attualmente solo i singoli valori di enumerazione. non verifica se una combinazione bit per bit è valida.

 

 

 
