---
description: Interfaccia originale per la comunicazione dei dati relativi a un oggetto vsglog.
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df19b1c717068749255af643c02cbdc82f1679e3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623487"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span id="vspixengine.ipixengine"></span>Interfaccia IPixEngine

Interfaccia originale per la comunicazione dei dati relativi a un oggetto vsglog.

## <a name="members"></a>Membri

**L'interfaccia IPixEngine** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixEngine** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

**L'interfaccia IPixEngine** include questi metodi.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></td><td style="text-align: left;"><p>Apre un log di grafica.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>Esecuzione (RunExperiment)</strong></a></td><td style="text-align: left;"><p>Esegue un esperimento.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></td><td style="text-align: left;"><p>Salva il log di grafica nel percorso specificato.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></td><td style="text-align: left;"><p>Non usato.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>Arresto</strong></a></td><td style="text-align: left;"><p>Arresta il motore.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
