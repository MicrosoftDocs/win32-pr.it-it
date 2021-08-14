---
description: Crea un enumeratore di informazioni sulle proprietà per ogni dispositivo wi-Windows image acquisition (WIA) 2.0 disponibile.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: Metodo IWiaDevMgr2::EnumDeviceInfo (Wia.h)
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
ms.openlocfilehash: 8b646c494d9793986373d45db2d89dfde91e744196d86d28aceab35874f504d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208723"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>Metodo IWiaDevMgr2::EnumDeviceInfo

Crea un enumeratore di informazioni sulle proprietà per ogni dispositivo wi-Windows image acquisition (WIA) 2.0 disponibile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica il tipo di dispositivi WIA 2.0 da enumerare.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ DEVINFO \_ ENUM \_ LOCAL**


</dt> <dd>

Vengono enumerati solo i dispositivi scanner attivi connessi in locale.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**ENUMERAZIONE DI WIA \_ DEVINFO \_ \_ ALL**


</dt> <dd>

Tutti i dispositivi vengono enumerati, sia in locale che in remoto, inclusi i dispositivi inattivi (disconnessi) e i dispositivi legacy solo STI.

</dd> </dl> </dd> <dt>

*ppIEnum* \[ out, retval\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Riceve l'indirizzo di un puntatore [**all'interfaccia IEnumWIA \_ DEV \_ INFO.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il **metodo IWiaDevMgr2::EnumDeviceInfo** crea un oggetto enumeratore che supporta l'interfaccia [**IEnumWIA \_ DEV \_ INFO.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) Il metodo archivia un puntatore **all'interfaccia IEnumWIA \_ DEV \_ INFO** nel parametro *ppIEnum*. Le applicazioni possono usare il puntatore a interfaccia **IEnumWIA \_ DEV \_ INFO** per enumerare le proprietà di ogni dispositivo WIA 2.0 collegato al computer dell'utente.

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro ppIEnum.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
