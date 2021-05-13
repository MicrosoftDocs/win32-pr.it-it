---
description: Il metodo Create dell'oggetto Wia crea una connessione al dispositivo WIA (Windows Image Acquisition) specificato e restituisce un oggetto Item che rappresenta il dispositivo.
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
ms.openlocfilehash: d22d45e473cec1d5186c300f97cbdb4661237ab9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841332"
---
# <a name="wiacreate-method"></a>Metodo Wia.Create

Il **metodo Create** dell'oggetto [**Wia**](-wia-wia.md) crea una connessione al dispositivo WIA (Windows Image Acquisition) specificato e restituisce un [**oggetto Item**](-wia-item.md) che rappresenta il dispositivo.

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

Se ha esito positivo, questo metodo restituisce un [**oggetto Item**](-wia-item.md) che rappresenta un dispositivo hardware WIA (un elemento radice).

## <a name="remarks"></a>Commenti

Il *parametro Device* specifica un oggetto [**DeviceInfo**](-wia-deviceinfo.md) passando l'oggetto stesso, il relativo indice da un oggetto raccolta o il valore della relativa [**proprietà Id.**](-wia-iwiadeviceinfo-id.md) Passare **Nothing** per visualizzare una finestra di dialogo che consente a un utente di selezionare un dispositivo.

## <a name="examples"></a>Esempio

Gli esempi DI VBScript seguenti illustrano l'uso del **metodo Create.**

Il primo esempio passa [**un oggetto DeviceInfo**](-wia-deviceinfo.md) al **metodo Create.** Si noti che il passaggio della proprietà [**Id**](-wia-iwiadeviceinfo-id.md) dell'oggetto determina esattamente lo stesso comportamento.


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



L'esempio successivo passa **Nothing** al **metodo Create** per visualizzare una finestra di dialogo che consente a un utente di selezionare un dispositivo.


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
| Client minimo supportato<br/> | Solo app desktop di Windows 2000 Professional e Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




