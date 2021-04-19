---
title: Mediacollection. getMediaAtom, metodo
description: Il metodo getMediaAtom recupera l'indice in corrispondenza del quale si trova un attributo specificato all'interno del set di attributi disponibili.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- Metodo getMediaAtom Windows Media Player
- Metodo getMediaAtom Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getMediaAtom
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327623"
---
# <a name="mediacollectiongetmediaatom-method"></a>Mediacollection. getMediaAtom, metodo

Il metodo **getMediaAtom** recupera l'indice in corrispondenza del quale si trova un attributo specificato all'interno del set di attributi disponibili.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**).

## <a name="remarks"></a>Commenti

Il numero di indice recuperato con questo metodo può essere passato al *supporto*. metodo **getItemInfoByAtom** per accedere ai valori di attributo. Questa tecnica è in genere più efficiente quando si lavora con playlist di grandi dimensioni anziché accedere a un valore di attributo in base al nome tramite *supporti*. **GetItemInfo** o *supporti*. **getItemInfoByType**.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getItemInfoByAtom**](media-getiteminfobyatom.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





