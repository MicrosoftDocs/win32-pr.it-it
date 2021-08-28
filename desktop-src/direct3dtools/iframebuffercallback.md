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
ms.openlocfilehash: 479796ebf225ceac4e93f429aa6b8412e3f86398
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628839"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span id="vspixengine.iframebuffercallback"></span>Interfaccia IFrameBufferCallback

Callback per restituire una destinazione di rendering. Il formato della destinazione di rendering restituita è R8G8B8A8 UNORM indipendentemente dal formato della destinazione di \_ rendering nel motore.

## <a name="members"></a>Membri

**L'interfaccia IFrameBufferCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IFrameBufferCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

**L'interfaccia IFrameBufferCallback** include questi metodi.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>Oggetto ResultCallback</strong></a></td><td style="text-align: left;"><p>Callback che notifica all'host le informazioni di framebuffer restituite dalla richiesta associata.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
