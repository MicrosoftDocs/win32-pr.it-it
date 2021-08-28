---
description: '<span id="vspixengine.ipipelinestagescallback"></span>Interfaccia IPipeLineStagesCallback: non usata. In precedenza un callback per i dati delle fasi della pipeline.'
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPipeLineStagesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2fc828d902f1daa3b2c0c75d2f22671d9bdec942
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787501"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span id="vspixengine.ipipelinestagescallback"></span>Interfaccia IPipeLineStagesCallback

Non usato. In precedenza un callback per i dati delle fasi della pipeline.

## <a name="members"></a>Membri

**L'interfaccia IPipeLineStagesCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPipeLineStagesCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

**L'interfaccia IPipeLineStagesCallback** include questi metodi.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Metodo</th><th >Descrizione</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></td><td ><p>Callback che notifica all'host le fasi della pipeline usate dalla chiamata di disegno della richiesta assocaited.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></td><td ><p>Callback che notifica all'host quali fasi della pipeline non sono in grado di restituire dati mesh per l'evento specificato nella richiesta associata.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></td><td ><p>Callback che notifica all'host delle fasi della pipeline le informazioni sulla mesh restituite dalla richiesta assocaited.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></td><td ><p>Callback che notifica all'host delle fasi della pipeline le informazioni sull'immagine restituite dalla richiesta assocaited.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
