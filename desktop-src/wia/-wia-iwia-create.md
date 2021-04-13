---
description: Il metodo create dell'oggetto WIA esegue una connessione al dispositivo Windows Image Acquisition (WIA) specificato e restituisce un oggetto Item che rappresenta il dispositivo.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Metodo WIA. Create
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
ms.openlocfilehash: 6a388ba2b3ee0506b093221275e34104e3f91bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529149"
---
# <a name="wiacreate-method"></a>Metodo WIA. Create

Il metodo **create** dell'oggetto [**WIA**](-wia-wia.md) esegue una connessione al dispositivo Windows Image Acquisition (WIA) specificato e restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dispositivo* \[ in\]
</dt> <dd>

Tipo: **Variant \** _

Specifica il dispositivo WIA a cui connettersi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *IWiaDispatchItem**

Se ha esito positivo, questo metodo restituisce un oggetto [**Item**](-wia-item.md) che rappresenta un dispositivo hardware WIA (un elemento radice).

## <a name="remarks"></a>Commenti

Il parametro *Device* specifica un oggetto [**deviceInfo**](-wia-deviceinfo.md) passando l'oggetto stesso, il relativo indice da un oggetto Collection o il valore della relativa proprietà [**ID**](-wia-iwiadeviceinfo-id.md) . **Non passare nulla** per visualizzare una finestra di dialogo che consente a un utente di selezionare un dispositivo.

## <a name="examples"></a>Esempio

Negli esempi VBScript seguenti viene illustrato l'utilizzo del metodo **create** .

Nel primo esempio viene passato un oggetto [**deviceInfo**](-wia-deviceinfo.md) al metodo **create** . Si noti che il passaggio della proprietà [**ID**](-wia-iwiadeviceinfo-id.md) dell'oggetto causa esattamente lo stesso comportamento.


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



Nell'esempio successivo, l'applicazione chiamante passa l'indice dell'oggetto [**deviceInfo**](-wia-deviceinfo.md) nella raccolta al metodo **create** .


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



Nell'esempio seguente non viene passato **alcun** valore al metodo **create** per visualizzare una finestra di dialogo che consente a un utente di selezionare un dispositivo.


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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




