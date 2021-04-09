---
description: Il metodo GetItemsFromUI dell'oggetto Item Visualizza una finestra di dialogo che consente a un utente di selezionare immagini e audio da trasferire da un dispositivo.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. GetItemsFromUI, metodo
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
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130019"
---
# <a name="itemgetitemsfromui-method"></a>Item. GetItemsFromUI, metodo

Il metodo **GetItemsFromUI** dell'oggetto [**Item**](-wia-item.md) Visualizza una finestra di dialogo che consente a un utente di selezionare immagini e audio da trasferire da un dispositivo.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **WiaFlag**](-wia-wiaflag.md)**

<dt>



  (0)


</dt> <dd>

Valore predefinito. \[in \] specifica il comportamento della finestra di dialogo. I valori validi per questo parametro sono identici a quelli per il parametro *è* del metodo [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .

</dd> </dl> </dd> <dt>

*Finalità* \[ in\]
</dt> <dd>

Tipo: **WiaIntent**

<dt>



  (0)


</dt> <dd>

Valore predefinito. \[in \] specifica il tipo di dati che l'immagine deve rappresentare. Per un elenco di valori per finalità immagine, vedere [**costanti per finalità di immagine**](-wia-imageintentconstants.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **ICollection**

Questo metodo restituisce una raccolta di oggetti [**Item**](-wia-item.md) che rappresentano gli elementi selezionati dall'utente. Se non è selezionato alcun elemento, l'insieme è vuoto.

## <a name="remarks"></a>Commenti

Per le applicazioni Microsoft Visual Basic, aggiungere un riferimento a "Windows Image Acquisition 1,01 Type Library".

Questo metodo si applica solo ai dispositivi (elementi radice). Il metodo restituisce una raccolta di oggetti [**Item**](-wia-item.md) che rappresentano le immagini o i clip audio selezionati dall'utente.

Se l'utente non seleziona elementi, il metodo restituisce una raccolta vuota.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo del metodo **GetItemsFromUI** per consentire a un utente di selezionare immagini da una finestra di dialogo.


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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




