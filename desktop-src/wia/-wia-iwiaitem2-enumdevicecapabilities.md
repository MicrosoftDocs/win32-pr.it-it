---
description: Crea un enumeratore utilizzato per verificare i comandi e gli eventi supportati da un dispositivo wi-Windows Image Acquisition (WIA) 2.0.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: Metodo IWiaItem2::EnumDeviceCapabilities (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6748966beaa3bf16f668c4b8b0de60a4302ebcf514f06a3d588999d5faebaf3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450461"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>Metodo IWiaItem2::EnumDeviceCapabilities

Crea un enumeratore utilizzato per verificare i comandi e gli eventi supportati da un dispositivo wi-Windows Image Acquisition (WIA) 2.0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica un flag che seleziona il tipo di funzionalità da enumerare. Si tratta di uno dei valori seguenti.

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**COMANDI DEL DISPOSITIVO WIA \_ \_**


</dt> <dd>

Enumerare i comandi del dispositivo.

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**EVENTI DEL DISPOSITIVO WIA \_ \_**


</dt> <dd>

Enumerare gli eventi del dispositivo.

</dd> </dl> </dd> <dt>

*ppIEnumWIA \_ DEV \_ CAPS* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Riceve un puntatore [**all'interfaccia IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) creata da questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene usato per creare un oggetto enumeratore per ottenere il set di comandi ed eventi supportati da un dispositivo WIA 2.0. Il *parametro lFlags* viene usato per specificare i tipi di funzionalità del dispositivo da enumerare. Il **metodo IWiaItem2::EnumDeviceCapabilities** archivia l'indirizzo dell'interfaccia dell'oggetto enumeratore nel parametro *PPIEnumWIA \_ DEV \_ CAPS.*

Questo metodo può essere chiamato solo sull'elemento radice degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) di un albero dei dispositivi.

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il parametro *PPIEnumWIA \_ DEV \_ CAPS.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
