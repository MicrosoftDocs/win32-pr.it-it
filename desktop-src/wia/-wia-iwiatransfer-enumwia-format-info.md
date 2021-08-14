---
description: Crea un enumeratore per i formati di trasferimento supportati Windows dispositivo WIA (Image Acquisition) 2.0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: Metodo IWiaTransfer::EnumWIA_FORMAT_INFO (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 5e497d389646249c03bfaa4ac8625ce2a440b97f4ff6b8c0b0942ec957d0901e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669476"
---
# <a name="iwiatransferenumwia_format_info-method"></a>Metodo IWiaTransfer::EnumWIA \_ FORMAT \_ INFO

Crea un enumeratore per i formati di trasferimento supportati Windows dispositivo WIA (Image Acquisition) 2.0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIEnum* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

Indirizzo del puntatore [**all'interfaccia IEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) per l'enumeratore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore di interfaccia ricevuto tramite il *parametro ppIEnum.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
