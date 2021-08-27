---
description: Richiesta di intersezioni di cronologia pixel e primitive separatamente.
MS-HAID: vspixengine.IPixelHistoryRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixelHistoryRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B62A9EBA-4497-4825-A2F1-285A4AD45012
api_name:
- IPixelHistoryRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e4fc6c450a2ac31dc364ed20f4eb466ca0ae4d99
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622547"
---
# <a name="span-idvspixengineipixelhistoryrequest2spanipixelhistoryrequest2-interface"></a><span id="vspixengine.ipixelhistoryrequest2"></span>Interfaccia IPixelHistoryRequest2

Richiesta di intersezioni di cronologia pixel e primitive separatamente.

## <a name="members"></a>Membri

**L'interfaccia IPixelHistoryRequest2** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixelHistoryRequest2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

**L'interfaccia IPixelHistoryRequest2** include questi metodi.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></td><td style="text-align: left;"><p>Richiede un elenco di eventi che causano una modifica nel pixel, nella destinazione di rendering/UAV e nel frame specificati.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></td><td style="text-align: left;"><p>Richiede un elenco di primitive da una determinata intersezione. Per altre informazioni, vedere la funzione membro RequestIntersections.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
