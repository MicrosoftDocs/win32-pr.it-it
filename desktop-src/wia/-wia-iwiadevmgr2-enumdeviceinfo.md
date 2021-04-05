---
description: Crea un enumeratore di informazioni sulle proprietà per ogni dispositivo Windows Image Acquisition (WIA) 2,0 disponibile.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'Metodo IWiaDevMgr2:: EnumDeviceInfo (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752839"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>Metodo IWiaDevMgr2:: EnumDeviceInfo

Crea un enumeratore di informazioni sulle proprietà per ogni dispositivo Windows Image Acquisition (WIA) 2,0 disponibile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica il tipo di dispositivi WIA 2,0 da enumerare.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**\_ \_ enumerazione locale WIA \_ DEVINFO**


</dt> <dd>

Vengono enumerati solo i dispositivi scanner attivi connessi localmente.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ DEVINFO \_ enum \_ All**


</dt> <dd>

Tutti i dispositivi vengono enumerati, sia localmente che remoti, inclusi i dispositivi inattivi (disconnessi) e i dispositivi solo STI legacy.

</dd> </dl> </dd> <dt>

*ppIEnum* \[ out, retval\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Riceve l'indirizzo di un puntatore all'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo **IWiaDevMgr2:: EnumDeviceInfo** crea un oggetto enumeratore che supporta l'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Il metodo archivia un puntatore all'interfaccia **IEnumWIA \_ dev \_ info** nel parametro *ppIEnum*. Le applicazioni possono usare il puntatore all'interfaccia **IEnumWIA \_ dev \_ info** per enumerare le proprietà di ogni dispositivo WIA 2,0 collegato al computer dell'utente.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnum* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
