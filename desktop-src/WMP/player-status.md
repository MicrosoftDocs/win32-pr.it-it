---
title: Player.status
description: La proprietà status recupera un valore che indica lo stato di Windows Media Player.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Player.status Windows Media Player
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03ef010bfcb5ee936183724331e97fac5d6f5912d87c5281a55106519c104e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572050"
---
# <a name="playerstatus"></a>Player.status

La **proprietà status** recupera un valore che indica lo stato di Windows Media Player.

## <a name="syntax"></a>Sintassi

*lettore* . **stato**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola lettura.

## <a name="remarks"></a>Commenti

I valori contenuti in questa proprietà sono soggetti a modifiche in qualsiasi momento e devono essere usati solo a scopo di visualizzazione.

**L'evento StatusChange** viene generato ogni volta che questa proprietà cambia valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 7.0 o versione successiva.<br/>                                      |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Evento Player.StatusChange**](player-player-statuschange.md)
</dt> </dl>

 

 





