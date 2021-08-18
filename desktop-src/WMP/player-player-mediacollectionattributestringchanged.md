---
title: Evento Player.MediaCollectionAttributeStringChanged
description: L'evento MediaCollectionAttributeStringChanged si verifica quando viene modificato un valore di attributo nella libreria. | Evento Player.MediaCollectionAttributeStringChanged
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Evento MediaCollectionAttributeStringChanged Windows Media Player
- Classe di evento MediaCollectionAttributeStringChanged Windows Media Player , Player
- Classe Player Windows Media Player, evento MediaCollectionAttributeStringChanged
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9435be90761abf88927789fad4380172f0ef6f31427848195d3aa14ea4112cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747397"
---
# <a name="playermediacollectionattributestringchanged-event"></a>Evento Player.MediaCollectionAttributeStringChanged

**L'evento MediaCollectionAttributeStringChanged** si verifica quando viene modificato un valore di attributo nella libreria.

## <a name="syntax"></a>Sintassi


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Stringa** che specifica il nome dell'attributo. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di Windows Media Player [sugli attributi.](attribute-reference.md)

</dd> <dt>

*bstrOldAttribVal* 
</dt> <dd>

**Stringa** che specifica il valore precedente dell'attributo.

</dd> <dt>

*bstrNewAttribVal* 
</dt> <dd>

**Stringa** che specifica il nuovo valore dell'attributo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando un utente modifica i metadati della libreria, **l'oggetto MediaCollection** viene aggiornato e questo evento viene generato per ogni attributo modificato.

Il valore dei parametri dell'evento viene specificato da Windows Media Player e può essere accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

**Windows Media Player 10 Mobile:** Questo evento non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





