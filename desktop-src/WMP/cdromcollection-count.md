---
title: Cdromcollection. Count
description: La proprietà Count recupera il numero di unità CD e DVD disponibili nel sistema.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- Windows Media Player cdromcollection. Count
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333136"
---
# <a name="cdromcollectioncount"></a>Cdromcollection. Count

La proprietà **count** Recupera il numero di unità CD e DVD disponibili nel sistema.

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Le unità DVD-ROM vengono conteggiate esattamente come le unità CD. Tuttavia, il controllo Media Player Windows supporta solo la funzionalità DVD per Windows XP o sistemi operativi successivi. In genere, le unità DVD possono riprodurre supporti CD, ma le unità CD non possono riprodurre supporti DVD.

**Windows Media Player 10 Mobile:** Questo metodo restituisce sempre 0.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato *cdromcollection*. **conteggio** per visualizzare il numero di unità CD e DVD disponibili nel computer dell'utente. L'oggetto Player è stato creato con ID = "Player".


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto cdromcollection**](cdromcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





