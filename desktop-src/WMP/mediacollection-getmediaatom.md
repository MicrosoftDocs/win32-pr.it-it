---
title: Metodo MediaCollection.getMediaAtom
description: Il metodo getMediaAtom recupera l'indice in corrispondenza del quale risiede un attributo specificato all'interno del set di attributi disponibili.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- Metodo getMediaAtom Windows Media Player
- Metodo getMediaAtom Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player, metodo getMediaAtom
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
ms.openlocfilehash: 8f537b759516d5fa0f382d0c72aabbc0edb836ad8e4ae6d7f210d012fa19ea60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837204"
---
# <a name="mediacollectiongetmediaatom-method"></a>Metodo MediaCollection.getMediaAtom

Il **metodo getMediaAtom** recupera l'indice in corrispondenza del quale risiede un attributo specificato all'interno del set di attributi disponibili.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ Pollici\]
</dt> <dd>

**Stringa contenente** il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di riferimento Windows Media Player [attributi.](attribute-reference.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**).

## <a name="remarks"></a>Commenti

Il numero di indice recuperato con questo metodo può essere passato all'oggetto *Media.* **Metodo getItemInfoByAtom** per accedere ai valori degli attributi. Questa tecnica è in genere più efficiente quando si lavora con playlist di grandi dimensioni rispetto all'accesso a un valore di attributo in base al nome tramite *Media*. **getItemInfo** o *Media.* **getItemInfoByType**.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.getItemInfoByAtom**](media-getiteminfobyatom.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





