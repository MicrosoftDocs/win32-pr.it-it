---
title: Player. Remote
description: La proprietà Remote recupera un valore che indica se il controllo Media Player di Windows è in esecuzione in modalità remota.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Media Player Windows Player. Remote
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c8d97ba212e032db16b43299d2a3a8a836f9b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326006"
---
# <a name="playerisremote"></a>Player. Remote

La proprietà **Remote** recupera un valore che indica se il controllo Media Player di Windows è in esecuzione in modalità remota.

## <a name="syntax"></a>Sintassi

*Player* . **Remote**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** di sola lettura.



| Valore | Descrizione                                   |
|-------|-----------------------------------------------|
| true  | Il controllo Player viene eseguito in modalità remota. |
| false | Il controllo Player viene eseguito in modalità locale.  |



 

## <a name="remarks"></a>Commenti

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





