---
title: Cdrom. driveSpecifier
description: La proprietà driveSpecifier recupera la lettera dell'unità CD o DVD.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Media Player Windows cdrom. driveSpecifier
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517523"
---
# <a name="cdromdrivespecifier"></a>Cdrom. driveSpecifier

La proprietà **driveSpecifier** recupera la lettera dell'unità CD o DVD.

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura.

## <a name="remarks"></a>Commenti

In genere, le unità DVD possono riprodurre supporti CD, ma le unità CD non possono riprodurre supporti DVD. Questa proprietà recupera un identificatore di unità per un indice di unità in base zero nell'intervallo recuperato utilizzando *cdromcollection*. **conteggio**. Il valore recuperato assume il formato *x*:, dove *x* rappresenta la lettera di unità.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato *CDROM*. **driveSpecifier** per riempire un'area di testo HTML denominata testo con un elenco delimitato da virgole di unità CD e DVD disponibili. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Versione<br/>                  | Windows Media Player versione 7,0 o successiva<br/>                               |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto cdrom**](cdrom-object.md)
</dt> <dt>

[**Cdromcollection. Count**](cdromcollection-count.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





