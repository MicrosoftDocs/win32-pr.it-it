---
description: Il metodo GetItemsFromUI dell'oggetto Item visualizza una finestra di dialogo che consente a un utente di selezionare immagini e audio da trasferire da un dispositivo.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Metodo Item.GetItemsFromUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a954dbefec9728d2d6f595144ba3991ab4f7b3a1ded77fdf7e3ca5407be70d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669713"
---
# <a name="itemgetitemsfromui-method"></a>Metodo Item.GetItemsFromUI

Il **metodo GetItemsFromUI** dell'oggetto [**Item**](-wia-item.md) visualizza una finestra di dialogo che consente a un utente di selezionare immagini e audio da trasferire da un dispositivo.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **WiaFlag**](-wia-wiaflag.md)**

<dt>



  (0)


</dt> <dd>

Valore predefinito. \[in \] Specifica il comportamento della finestra di dialogo. I valori validi per questo parametro sono gli stessi del parametro *lFlags* del [**metodo DeviceDlg.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)

</dd> </dl> </dd> <dt>

*Finalità* \[ Pollici\]
</dt> <dd>

Tipo: **WiaIntent**

<dt>



  (0)


</dt> <dd>

Valore predefinito. \[in \] specifica il tipo di dati che l'immagine deve rappresentare. Per un elenco dei valori di finalità dell'immagine, vedere [**Costanti finalità immagine**](-wia-imageintentconstants.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **ICollection**

Questo metodo restituisce una raccolta di [**oggetti Item**](-wia-item.md) che rappresentano gli elementi selezionati dall'utente. Se non è selezionato alcun elemento, la raccolta è vuota.

## <a name="remarks"></a>Commenti

Per le Visual Basic Microsoft, aggiungere un riferimento a "Windows Image Acquisition 1.01 Type Library".

Questo metodo si applica solo ai dispositivi (elementi radice). Il metodo restituisce una raccolta di [**oggetti Item**](-wia-item.md) che rappresentano le immagini o i clip audio selezionati dall'utente.

Se l'utente non seleziona alcun elemento, il metodo restituisce una raccolta vuota.

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso del **metodo GetItemsFromUI** per consentire a un utente di selezionare immagini da una finestra di dialogo.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




