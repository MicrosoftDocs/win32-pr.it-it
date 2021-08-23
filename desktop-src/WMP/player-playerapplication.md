---
title: Player.playerApplication
description: La proprietà playerApplication recupera l'oggetto PlayerApplication quando è in esecuzione un controllo Windows Media Player remoto.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Player.playerApplication Windows Media Player
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c47400fcba1cb1cd1679e747d4fdd49b155df921ec33a721f74df2ec25259600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995851"
---
# <a name="playerplayerapplication"></a>Player.playerApplication

La **proprietà playerApplication** recupera l'oggetto **PlayerApplication** quando un controllo Windows Media Player remoto è in esecuzione.

## <a name="syntax"></a>Sintassi

**playerApplication**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto **PlayerApplication** di sola lettura o il valore Null.

## <a name="remarks"></a>Commenti

Questa proprietà viene usata solo quando si esegue la comunicazione remota Windows Media Playercontrol. Se il valore è Null, il Windows Media Playercontrol non è incorporato in modalità remota.

Questa proprietà è accessibile solo nel codice C++ o nel codice script nelle skin tramite la variabile globale playerApplication.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi globali**](global-attributes.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Oggetto PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





