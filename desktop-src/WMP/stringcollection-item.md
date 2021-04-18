---
title: Metodo StringCollection. Item
description: Il metodo Item recupera la stringa in corrispondenza dell'indice specificato.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- Metodo Item Media Player Windows
- elemento Method Media Player di Windows, classe StringCollection
- StringCollection (classe) Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324458"
---
# <a name="stringcollectionitem-method"></a>Metodo StringCollection. Item

Il metodo **Item** recupera la stringa in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che contiene l'indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa**.

## <a name="remarks"></a>Commenti

L'oggetto **StringCollection** viene utilizzato per recuperare il set di valori disponibili per un attributo. Ad esempio, *mediacollection*. il metodo **getAttributeStringCollection** può essere usato per recuperare un oggetto **StringCollection** che rappresenta tutti i valori per l'attributo Genre all'interno del tipo di supporto audio. La proprietà **Item** può quindi essere usata per scorrere tutti i valori possibili per l'attributo Genre.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mediacollection. getAttributeStringCollection**](mediacollection-getattributestringcollection.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection (oggetto)**](stringcollection-object.md)
</dt> </dl>

 

 





