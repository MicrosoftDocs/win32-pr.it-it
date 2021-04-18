---
description: Crea un enumeratore per i formati di trasferimento supportati dal dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'Metodo IWiaTransfer:: EnumWIA_FORMAT_INFO (WIA. h)'
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
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307354"
---
# <a name="iwiatransferenumwia_format_info-method"></a>\_Metodo informazioni sul formato IWiaTransfer:: EnumWIA \_

Crea un enumeratore per i formati di trasferimento supportati dal dispositivo Windows Image Acquisition (WIA) 2,0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIEnum* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ \_ info Format**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

Indirizzo del puntatore all'interfaccia [**IEnumWIA \_ Format \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) per l'enumeratore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore a interfaccia ricevuto tramite il parametro *ppIEnum* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
