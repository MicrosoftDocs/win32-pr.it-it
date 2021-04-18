---
title: PlayerApplication.hasDisplay
description: La proprietà hasDisplay recupera un valore che indica se il video può essere visualizzato tramite il controllo lettore remoto.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- Media Player Windows PlayerApplication. hasDisplay
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
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327050"
---
# <a name="playerapplicationhasdisplay"></a>PlayerApplication.hasDisplay

La proprietà **hasDisplay** recupera un valore che indica se il video può essere visualizzato tramite il controllo lettore remoto.

## <a name="syntax"></a>Sintassi

*playerApplication*. **hasDisplay**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** di sola lettura.

## <a name="remarks"></a>Commenti

Questa proprietà viene utilizzata solo per la comunicazione remota del controllo Media Player di Windows.

È possibile eseguire contemporaneamente più controlli Media Player di Windows, ma i video possono essere visualizzati solo in una posizione alla volta, nella modalità completa del lettore o in uno dei controlli di Windows Media Player remoto. Usare questa proprietà per determinare se il controllo corrente è quello tramite il quale è possibile visualizzare il video.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





