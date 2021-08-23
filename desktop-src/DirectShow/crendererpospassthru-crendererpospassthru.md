---
description: 'Costruttore CRendererPosPassThru.CRendererPosPassThru : metodo costruttore.'
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: Costruttore CRendererPosPassThru.CRendererPosPassThru (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5fc61250f75cc8a49d699a5f3bee97b707c59e134864a23eac9887dfb34618f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953800"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a>Costruttore CRendererPosPassThru.CRendererPosPassThru

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore al nome dell'oggetto, a scopo di debug. Allocare questo parametro nella memoria statica.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Ignorato.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di input del filtro.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




