---
description: Il metodo Create dell'oggetto Wia effettua una connessione al dispositivo wia specificato Windows Image Acquisition (WIA) e restituisce un oggetto Item che rappresenta il dispositivo.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Metodo Wia.Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a4056354992010d3d213ed619b7460e12c800630ca38fb17acb6d7677fe842a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814051"
---
# <a name="wiacreate-method"></a>Metodo Wia.Create

Il **metodo Create** dell'oggetto [**Wia**](-wia-wia.md) effettua una connessione al dispositivo Windows Image Acquisition (WIA) specificato e restituisce un [**oggetto Item**](-wia-item.md) che rappresenta il dispositivo.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dispositivo* \[ Pollici\]
</dt> <dd>

Tipo: **\* VARIANT**

Specifica il dispositivo WIA a cui connettersi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **IWiaDispatchItem**

Se ha esito positivo, questo metodo restituisce [**un oggetto Item**](-wia-item.md) che rappresenta un dispositivo hardware WIA (un elemento radice).

## <a name="remarks"></a>Commenti

Il *parametro Device* specifica un oggetto [**DeviceInfo**](-wia-deviceinfo.md) passando l'oggetto stesso, il relativo indice da un oggetto raccolta o il valore della relativa proprietà [**Id.**](-wia-iwiadeviceinfo-id.md) Non **passare nulla** per visualizzare una finestra di dialogo che consente a un utente di selezionare un dispositivo.

## <a name="examples"></a>Esempio

Gli esempi di VBScript seguenti illustrano l'uso del **metodo Create.**

Il primo esempio passa [**un oggetto DeviceInfo**](-wia-deviceinfo.md) al **metodo Create.** Si noti che il passaggio della proprietà [**Id**](-wia-iwiadeviceinfo-id.md) dell'oggetto causa esattamente lo stesso comportamento.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



Nell'esempio successivo l'applicazione chiamante passa l'indice [**dell'oggetto DeviceInfo**](-wia-deviceinfo.md) nella raccolta al **metodo Create.**


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



L'esempio seguente passa **Nothing** al **metodo Create** per visualizzare una finestra di dialogo che consente a un utente di selezionare un dispositivo.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




