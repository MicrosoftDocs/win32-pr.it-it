---
description: Crea un albero gerarchico di oggetti IWiaItem2 per Windows dispositivo WIA (Image Acquisition) 2.0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: Metodo IWiaDevMgr2::CreateDevice (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a40267e77671b807f0e6969845a3a5a7096694e4f4e7978467ee9ca5909284d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965730"
---
# <a name="iwiadevmgr2createdevice-method"></a>Metodo IWiaDevMgr2::CreateDevice

Crea un albero gerarchico [**di oggetti IWiaItem2**](-wia-iwiaitem2.md) per Windows dispositivo WIA (Image Acquisition) 2.0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*bstrDeviceID* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica l'identificatore univoco del dispositivo WIA 2.0.

</dd> <dt>

*ppWiaItem2Root* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore [**all'interfaccia IWiaItem2**](-wia-iwiaitem2.md) dell'elemento radice nell'albero gerarchico per il dispositivo WIA 2.0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Le applicazioni usano il metodo **IWiaDevMgr2::CreateDevice** per creare un oggetto dispositivo per i dispositivi WIA 2.0 specificati dal parametro bstrDeviceID. Quando viene restituito, il metodo **IWiaDevMgr2::CreateDevice** archivia un indirizzo di un puntatore nel parametro *ppWiaItem2Root*, che punta all'elemento radice dell'albero degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) creati da **IWiaDevMgr2::CreateDevice**. Le applicazioni possono usare questo albero di oggetti per controllare e recuperare dati dal dispositivo WIA 2.0.

Le applicazioni devono [chiamare il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori ricevuti tramite il *parametro ppWiaItem2Root.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
