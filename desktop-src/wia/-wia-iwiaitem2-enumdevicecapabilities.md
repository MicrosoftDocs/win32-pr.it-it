---
description: Crea un enumeratore usato per verificare i comandi e gli eventi supportati da un dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'Metodo IWiaItem2:: EnumDeviceCapabilities (WIA. h)'
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
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526467"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>Metodo IWiaItem2:: EnumDeviceCapabilities

Crea un enumeratore usato per verificare i comandi e gli eventi supportati da un dispositivo Windows Image Acquisition (WIA) 2,0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica un flag che seleziona il tipo di funzionalità da enumerare. È uno dei valori seguenti.

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**\_comandi del dispositivo WIA \_**


</dt> <dd>

Enumera i comandi del dispositivo.

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_eventi del dispositivo WIA \_**


</dt> <dd>

Enumerare gli eventi del dispositivo.

</dd> </dl> </dd> <dt>

*ppIEnumWIA \_ DEV \_ Caps* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Riceve un puntatore all'interfaccia [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) creata da questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene usato per creare un oggetto enumeratore per ottenere il set di comandi ed eventi supportati da un dispositivo WIA 2,0. Il parametro *è* viene usato per specificare i tipi di funzionalità del dispositivo da enumerare. Il metodo **IWiaItem2:: EnumDeviceCapabilities** archivia l'indirizzo dell'interfaccia dell'oggetto enumeratore nel parametro *ppIEnumWIA \_ dev \_ Caps* .

Questo metodo può essere chiamato solo sull'elemento radice degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) di un albero del dispositivo.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnumWIA \_ dev \_ Caps* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
