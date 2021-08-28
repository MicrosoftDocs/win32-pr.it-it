---
description: Callback dal motore che indica che è stata completata l'analisi di tutti i nuovi frame aggiunti al log.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia INewFramesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8b5e27183461ca1eb0e214000551e18c08d2914f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631419"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span id="vspixengine.inewframescallback"></span>Interfaccia INewFramesCallback

Callback dal motore che indica che è stata completata l'analisi di tutti i nuovi frame aggiunti al log.

## <a name="members"></a>Membri

**L'interfaccia INewFramesCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INewFramesCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

Questi metodi sono disponibili nell'interfaccia **INewFramesCallback.**

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></td><td style="text-align: left;"><p>Callback che notifica all'host che tutte le richieste sono state annullate.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></td><td style="text-align: left;"><p>Callback che notifica all'host di una richiesta annullata.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></td><td style="text-align: left;"><p>Callback che notifica all'host di una richiesta annullata usando un cookie che identifica in modo univoco la richiesta.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></td><td style="text-align: left;"><p>Callback che notifica all'host che sono disponibili nuovi frame per l'elaborazione.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
