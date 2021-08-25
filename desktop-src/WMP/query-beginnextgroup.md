---
title: Metodo Query.beginNextGroup
description: Il metodo beginNextGroup avvia un nuovo gruppo di condizioni. | Metodo Query.beginNextGroup
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- Metodo beginNextGroup Windows Media Player
- Metodo beginNextGroup Windows Media Player , classe Query
- Query class Windows Media Player metodo beginNextGroup
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
ms.openlocfilehash: 1d12f8e37c32b83afb3e518deda09643033c7f396d8c52a2898893a01dc930d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861851"
---
# <a name="querybeginnextgroup-method"></a>Metodo Query.beginNextGroup

Il **metodo beginNextGroup** avvia un nuovo gruppo di condizioni.

## <a name="syntax"></a>Sintassi


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

L'inizio di un nuovo gruppo di condizioni implica che il gruppo di condizioni corrente è stato completato. Il nuovo gruppo di condizioni viene sempre concatenato al gruppo di condizioni precedente usando la logica OR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MediaCollection.createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Oggetto Query**](query-object.md)
</dt> <dt>

[**Query.addCondition**](query-addcondition.md)
</dt> </dl>

 

 





