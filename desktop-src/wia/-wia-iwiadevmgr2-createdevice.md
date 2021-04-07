---
description: Crea un albero gerarchico di oggetti IWiaItem2 per un dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'Metodo IWiaDevMgr2:: CreateDevice (WIA. h)'
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
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881897"
---
# <a name="iwiadevmgr2createdevice-method"></a>Metodo IWiaDevMgr2:: CreateDevice

Crea un albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) per un dispositivo Windows Image Acquisition (WIA) 2,0.

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

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> <dt>

*bstrDeviceID* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica l'identificatore univoco del dispositivo WIA 2,0.

</dd> <dt>

*ppWiaItem2Root* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento radice nell'albero gerarchico per il dispositivo WIA 2,0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Le applicazioni usano il metodo **IWiaDevMgr2:: CreateDevice** per creare un oggetto dispositivo per i dispositivi WIA 2,0 specificati dal parametro bstrDeviceID. Quando restituisce, il metodo **IWiaDevMgr2:: CreateDevice** archivia un indirizzo di un puntatore nel parametro *ppWiaItem2Root*, che fa riferimento all'elemento radice della struttura ad albero di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) creati da **IWiaDevMgr2:: CreateDevice**. Le applicazioni possono usare questo albero di oggetti per controllare e recuperare i dati dal dispositivo WIA 2,0.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori ricevuti tramite il parametro *ppWiaItem2Root* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
