---
description: Interfaccia per la comunicazione remota dei dati relativi a un vsglog.
MS-HAID: vspixengine.IPeerToPeerEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPeerToPeerEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C6C4783F-ED46-47C2-98BB-C618897F8FF8
api_name:
- IPeerToPeerEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e654d7dd31aa003dbd97af9cafb6831e914f2f7
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623317"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span id="vspixengine.ipeertopeerengine"></span>Interfaccia IPeerToPeerEngine

Interfaccia per la comunicazione remota dei dati relativi a un vsglog.

## <a name="members"></a>Membri

**L'interfaccia IPeerToPeerEngine** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPeerToPeerEngine** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

Questi metodi sono disponibili nell'interfaccia **IPeerToPeerEngine.**

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></td><td style="text-align: left;"><p>Annulla una richiesta precedente per configurare una connessione remota.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></td><td style="text-align: left;"><p>Ottiene l'indirizzo dell'endpoint di un motore remoto.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></td><td style="text-align: left;"><p>Imposta l'indirizzo dell'endpoint utilizzato per connettersi a un motore remoto.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
