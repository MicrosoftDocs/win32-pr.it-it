---
description: Ottiene il Windows di anteprima wi-to-image (WIA) 2.0.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: Metodo IWiaItem2::GetPreviewComponent (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3ac3705b4be60ce53fee411df1142fb64bbd1c393864b644e260829080be8f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450431"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>Metodo IWiaItem2::GetPreviewComponent

Ottiene il Windows di anteprima wi-to-image (WIA) 2.0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Non usato. Impostare su 0.

</dd> <dt>

*ppWiaPreview* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***

Restituisce l'indirizzo di un puntatore [**all'interfaccia IWiaPreview**](-wia-iwiapreview.md) del componente di anteprima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Usare questa funzione per restituire un puntatore all'indirizzo del componente di anteprima di WIA 2.0 per qualsiasi oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero di oggetti di un dispositivo hardware WIA 2.0.

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro ppWiaPreview.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IWiaPreview**](-wia-iwiapreview.md)
</dt> </dl>

 

 
