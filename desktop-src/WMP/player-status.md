---
title: Player. status
description: La proprietà Status recupera un valore che indica lo stato di Windows Media Player.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Player. status Windows Media Player
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
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324825"
---
# <a name="playerstatus"></a>Player. status

La proprietà **status** recupera un valore che indica lo stato di Windows Media Player.

## <a name="syntax"></a>Sintassi

*Player* . **stato** di

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola lettura.

## <a name="remarks"></a>Commenti

I valori contenuti in questa proprietà sono soggetti a modifiche in qualsiasi momento e devono essere utilizzati solo a scopo di visualizzazione.

L'evento **StatusChange** viene generato ogni volta che questa proprietà cambia valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 7,0 o versione successiva.<br/>                                      |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Evento Player. StatusChange**](player-player-statuschange.md)
</dt> </dl>

 

 





