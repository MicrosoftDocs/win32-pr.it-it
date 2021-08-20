---
description: Il metodo Create dell'oggetto DeviceInfo crea una connessione al dispositivo wia (Windows Image Acquisition) specificato dall'oggetto DeviceInfo e restituisce un oggetto Item che rappresenta il dispositivo.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: Metodo DeviceInfo.Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: bf0ff85733e71ce9425ae8176d9f6d0b97a3c85d0c4892145c112e6f42dd7036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670234"
---
# <a name="deviceinfocreate-method"></a>Metodo DeviceInfo.Create

Il **metodo Create** dell'oggetto [**DeviceInfo**](-wia-deviceinfo.md) crea una connessione al dispositivo wia (Windows Image Acquisition) specificato dall'oggetto **DeviceInfo** e restituisce un [**oggetto Item**](-wia-item.md) che rappresenta il dispositivo.

## <a name="syntax"></a>Sintassi


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **IWiaDispatchItem**

Questo metodo restituisce [**l'oggetto Item**](-wia-item.md) che rappresenta il dispositivo creato.

## <a name="remarks"></a>Commenti

Usare il **metodo Create** per creare una connessione a un dispositivo hardware WIA dopo l'enumerazione della [**raccolta Devices.**](-wia-iwia-devices.md) Il metodo restituisce un [**oggetto Item**](-wia-item.md) che rappresenta il dispositivo (un elemento radice).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'uso del **metodo Create.**


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




