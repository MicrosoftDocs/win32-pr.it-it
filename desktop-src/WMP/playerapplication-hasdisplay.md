---
title: PlayerApplication.hasDisplay
description: La proprietà hasDisplay recupera un valore che indica se il video può essere visualizzato tramite il controllo lettore remoto.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication.hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cffddc08c154ced6d7cb72b18642b5ebb4960e539e5682d1cf6e8518b74831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747360"
---
# <a name="playerapplicationhasdisplay"></a>PlayerApplication.hasDisplay

La **proprietà hasDisplay** recupera un valore che indica se il video può essere visualizzato tramite il controllo lettore remoto.

## <a name="syntax"></a>Sintassi

*playerApplication*. **hasDisplay**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un valore booleano **di sola lettura.**

## <a name="remarks"></a>Commenti

Questa proprietà viene utilizzata solo quando si esegue la comunicazione remota del Windows Media Player remoto.

Diversi Windows Media Player possono essere eseguiti in modalità remota contemporaneamente, ma il video può essere visualizzato solo in una posizione alla volta, nella modalità completa del lettore o in uno dei controlli Windows Media Player remoto. Usare questa proprietà per determinare se il controllo corrente è quello tramite il quale è possibile visualizzare il video.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre **true.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





