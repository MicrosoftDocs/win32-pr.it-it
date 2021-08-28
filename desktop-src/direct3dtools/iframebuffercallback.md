---
description: Callback per restituire una destinazione di rendering. Il formato della destinazione di rendering restituita è R8G8B8A8 UNORM indipendentemente dal formato della destinazione di \_ rendering nel motore.
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IFrameBufferCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7705f055fe09839d1e4afe22a9d779ca859ec3ba
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786537"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span id="vspixengine.iframebuffercallback"></span>Interfaccia IFrameBufferCallback

Callback per restituire una destinazione di rendering. Il formato della destinazione di rendering restituita è R8G8B8A8 UNORM indipendentemente dal formato della destinazione di \_ rendering nel motore.

## <a name="members"></a>Membri

**L'interfaccia IFrameBufferCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IFrameBufferCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

Questi metodi sono disponibili nell'interfaccia **IFrameBufferCallback.**

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Metodo</th><th >Descrizione</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></td><td ><p>Callback che notifica all'host le informazioni framebuffer restituite dalla richiesta associata.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
