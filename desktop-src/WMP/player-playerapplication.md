---
title: Player. playerApplication
description: La proprietà playerApplication recupera l'oggetto PlayerApplication quando viene eseguito un controllo Media Player Windows remoto.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Player. playerApplication Windows Media Player
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
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327709"
---
# <a name="playerplayerapplication"></a>Player. playerApplication

La proprietà **playerApplication** recupera l'oggetto **playerApplication** quando viene eseguito un controllo Media Player Windows remoto.

## <a name="syntax"></a>Sintassi

**playerApplication**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto **PlayerApplication** di sola lettura o il valore null.

## <a name="remarks"></a>Commenti

Questa proprietà viene utilizzata solo quando si esegue la comunicazione remota di Windows Media playercontrol. Se il valore è null, Windows Media playercontrol non è incorporato in modalità remota.

Questa proprietà è accessibile solo nel codice C++ o nel codice di script nelle interfacce tramite la variabile globale playerApplication.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
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

 

 





