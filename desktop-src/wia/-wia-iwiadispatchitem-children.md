---
description: La proprietà Children dell'oggetto Item recupera una raccolta di oggetti Item. Gli elementi in questa raccolta rappresentano elementi che sono elementi figlio diretti di questo elemento nell'albero gerarchico. Di sola lettura.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Item. Children (proprietà)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308232"
---
# <a name="itemchildren-property"></a>Item. Children (proprietà)

La proprietà **Children** dell'oggetto [**Item**](-wia-item.md) recupera una raccolta di oggetti **Item** . Gli elementi in questa raccolta rappresentano elementi che sono elementi figlio diretti di questo elemento nell'albero gerarchico. Di sola lettura.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>Valore proprietà

Variabile che riceve gli oggetti.

## <a name="remarks"></a>Commenti

Usare questa proprietà per esplorare l'albero gerarchico di oggetti [**elemento**](-wia-item.md) che rappresentano un dispositivo, le cartelle e i file che risiedono nel dispositivo.

La proprietà **Children** è una raccolta di oggetti [**Item**](-wia-item.md) solo dal livello direttamente sotto questo oggetto **Item** nell'albero. Per spostarsi verso il basso nella struttura ad albero, usare questa proprietà in modo ricorsivo.

Se l'elemento non può o non contiene elementi figlio, questa proprietà restituisce una raccolta vuota.

> [!Note]  
> Questa raccolta è in base 0.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo della proprietà **Children** per recuperare ed enumerare una raccolta di elementi figlio di un dispositivo. Se il dispositivo è una fotocamera digitale, la raccolta contiene in genere elementi di cartelle e immagini. Se il dispositivo è uno scanner, la raccolta contiene in genere elementi che rappresentano i letti di analisi.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




