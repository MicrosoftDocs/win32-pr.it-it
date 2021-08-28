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
ms.openlocfilehash: 4c52f22108b4a1b9b8576518801fc5e9896f28fa
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787133"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span id="vspixengine.ipixengine5"></span>Interfaccia IPixEngine5

Estensioni all'interfaccia IPixEngine4 contenenti aggiunte per la visualizzazione delle trame.

## <a name="members"></a>Membri

**L'interfaccia IPixEngine5** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixEngine5** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

Questi metodi sono disponibili nell'interfaccia **IPixEngine5.**

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Metodo</th><th >Descrizione</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></td><td ><p>Libera una trama e invia una notifica all'host in modo asincrono.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></td><td ><p>Richiesta asincrona di caricamento dei dati dell'istogramma.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></td><td ><p>Carica una trama da un file e invia una notifica all'host in modo asincrono al completamento.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></td><td ><p>Carica una sezione di trama e invia una notifica asincrona all'host al completamento.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></td><td ><p>Legge un valore texel e restituisce il risultato all'host in modo asincrono.</p></td></tr><tr class="even"><td ><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></td><td ><p>Esegue il rendering di una trama in un file e restituisce il risultato all'host in modo asincrono.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></td><td ><p>Salva una trama.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
