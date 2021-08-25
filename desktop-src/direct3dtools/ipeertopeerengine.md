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
ms.openlocfilehash: 85c5ba2866412ff6e6378bbead625a14bf7f5435
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786937"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span id="vspixengine.ipeertopeerengine"></span>Interfaccia IPeerToPeerEngine

Interfaccia per la comunicazione remota dei dati relativi a un vsglog.

## <a name="members"></a>Membri

**L'interfaccia IPeerToPeerEngine** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPeerToPeerEngine** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

**L'interfaccia IPeerToPeerEngine** dispone di questi metodi.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Metodo</th><th >Descrizione</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></td><td ><p>Annulla una richiesta precedente per configurare una connessione remota.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></td><td ><p>Ottiene l'indirizzo endpoint di un motore remoto.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></td><td ><p>Imposta l'indirizzo endpoint usato per connettersi a un motore remoto.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
