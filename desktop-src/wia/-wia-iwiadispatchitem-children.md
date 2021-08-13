---
description: La proprietà Children dell'oggetto Item recupera una raccolta di oggetti Item. Gli elementi di questa raccolta rappresentano elementi che sono figli diretti di questo elemento nell'albero gerarchico. Di sola lettura.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Item.Children - proprietà
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
ms.openlocfilehash: 72ce5119a10adc6a902d5a675d3ec116a3db1852a88e47ed852284cf44edf2f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440730"
---
# <a name="itemchildren-property"></a>Item.Children - proprietà

La **proprietà Children** dell'oggetto [**Item**](-wia-item.md) recupera una raccolta di **oggetti Item.** Gli elementi di questa raccolta rappresentano elementi che sono figli diretti di questo elemento nell'albero gerarchico. Di sola lettura.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>Valore proprietà

Variabile che riceve gli oggetti .

## <a name="remarks"></a>Commenti

Usare questa proprietà per spostarsi nell'albero gerarchico degli oggetti [**Item**](-wia-item.md) che rappresentano un dispositivo, le cartelle e i file che risiedono nel dispositivo.

La **proprietà Children** è una raccolta di oggetti [**Item**](-wia-item.md) solo dal livello direttamente sotto questo oggetto **Item** nell'albero. Per spostarsi in altri livelli verso il basso nell'albero, usare questa proprietà in modo ricorsivo.

Se l'elemento non può o non dispone di elementi figlio, questa proprietà restituisce una raccolta vuota.

> [!Note]  
> Questa raccolta è in base 0.

 

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso della **proprietà Children** per recuperare ed enumerare una raccolta di elementi figlio di un dispositivo. Se il dispositivo è una fotocamera digitale, la raccolta contiene in genere elementi cartella e immagine. Se il dispositivo è uno scanner, la raccolta contiene in genere elementi che rappresentano la scansione dei letti.


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




