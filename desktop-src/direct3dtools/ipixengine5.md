---
description: Estensioni all'interfaccia IPixEngine4 contenenti aggiunte per la visualizzazione delle trame.
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixEngine5
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1bce07a91ae8b96ef715f2ffbe254c4e810d7f59272e357590ff5eb1a24fdc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282391"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span id="vspixengine.ipixengine5"></span>Interfaccia IPixEngine5

Estensioni all'interfaccia IPixEngine4 contenenti aggiunte per la visualizzazione delle trame.

## <a name="members"></a>Membri

**L'interfaccia IPixEngine5** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixEngine5** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

Questi metodi sono disponibili nell'interfaccia **IPixEngine5.**

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></td><td style="text-align: left;"><p>Libera una trama e invia una notifica all'host in modo asincrono.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></td><td style="text-align: left;"><p>Richiesta asincrona di caricamento dei dati dell'istogramma.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></td><td style="text-align: left;"><p>Carica una trama da un file e invia una notifica all'host in modo asincrono al completamento.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></td><td style="text-align: left;"><p>Carica una sezione di trama e invia una notifica asincrona all'host al completamento.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></td><td style="text-align: left;"><p>Legge un valore texel e restituisce il risultato all'host in modo asincrono.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></td><td style="text-align: left;"><p>Esegue il rendering di una trama in un file e restituisce il risultato all'host in modo asincrono.</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></td><td style="text-align: left;"><p>Salva una trama.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
