---
title: Player.isRemote
description: La proprietà isRemote recupera un valore che indica se il controllo Windows Media Player è in esecuzione in modalità remota.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Player.isRemote Windows Media Player
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
ms.openlocfilehash: 6afa0caf615563f4829f1a337f31521b1fb7dafd5ef6e2722f1d50c01dda1ba4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616691"
---
# <a name="playerisremote"></a>Player.isRemote

La **proprietà isRemote** recupera un valore che indica se il controllo Windows Media Player è in esecuzione in modalità remota.

## <a name="syntax"></a>Sintassi

*lettore* . **isRemote**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un valore booleano **di sola lettura.**



| Valore | Descrizione                                   |
|-------|-----------------------------------------------|
| true  | Il controllo Player è in esecuzione in modalità remota. |
| false | Il controllo Player è in esecuzione in modalità locale.  |



 

## <a name="remarks"></a>Commenti

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





