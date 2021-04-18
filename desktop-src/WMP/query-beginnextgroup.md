---
title: Metodo query. beginNextGroup
description: Il metodo beginNextGroup avvia un nuovo gruppo di condizioni. | Metodo query. beginNextGroup
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- Metodo beginNextGroup Windows Media Player
- Metodo beginNextGroup Media Player Windows, classe query
- Classe di query Windows Media Player, metodo beginNextGroup
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331220"
---
# <a name="querybeginnextgroup-method"></a>Metodo query. beginNextGroup

Il metodo **beginNextGroup** avvia un nuovo gruppo di condizioni.

## <a name="syntax"></a>Sintassi


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'inizio di un nuovo gruppo di condizioni implica il completamento del gruppo di condizioni corrente. Il nuovo gruppo di condizioni viene sempre concatenato al gruppo di condizioni precedente mediante la logica o.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mediacollection. createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**Mediacollection. getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Mediacollection. getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Oggetto query**](query-object.md)
</dt> <dt>

[**Query. addCondition**](query-addcondition.md)
</dt> </dl>

 

 





