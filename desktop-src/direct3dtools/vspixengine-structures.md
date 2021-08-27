---
description: Le strutture seguenti sono dichiarate in vspixengine.h.
MS-HAID: vspixengine.vspixengine\_structures
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Strutture dell'interfaccia di acquisizione diagnostica Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 97F142F6-FED1-4AF4-B9E3-BB1E30F3FAD2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 611a8112c1eb99c142c92f63f598e903352528f8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622287"
---
# <a name="span-idvspixenginevspixengine_structuresspandirect3d-diagnostics-capture-interface-structures"></a><span id="vspixengine.vspixengine_structures"></span>Strutture dell'interfaccia di acquisizione diagnostica Direct3D

Le strutture seguenti sono dichiarate in vspixengine.h.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In questa sezione

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Argomento</th><th>Descrizione</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/resourcepair"><strong>ResourcePair</strong></a></p></td><td><p>Rappresenta una risorsa condivisa codificata come stringa COM.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptorheaprecord"><strong>DescriptorHeapRecord</strong></a></p></td><td><p>Rappresenta le informazioni sull'heap del descrittore.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestageerror"><strong>PipeLineStageError</strong></a></p></td><td><p>Rappresenta un errore in una fase della pipeline.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pipelinestage"><strong>PipeLineStage</strong></a></p></td><td><p>Rappresenta una fase della pipeline, inclusi i dettagli dello shader usato.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/experimenttrigger"><strong>ExperimentTrigger</strong></a></p></td><td><p>Rappresenta le informazioni sul trigger dell'esperimento.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/packedcallpkg"><strong>PackedCallPkg</strong></a></p></td><td><p>Rappresenta un pacchetto di quattro chiamate.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/symbolserverinfo"><strong>SymbolServerInfo</strong></a></p></td><td><p>Rappresenta informazioni sul server di simboli di debug.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/callstackframe"><strong>CallStackFrame</strong></a></p></td><td><p>Rappresenta informazioni su un frame nell'oggetto callstack.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/sourcefileinfo"><strong>SourceFileInfo</strong></a></p></td><td><p>Rappresenta informazioni su un file di codice sorgente.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/summaryitem"><strong>SummaryItem</strong></a></p></td><td><p>Rappresenta informazioni di riepilogo su un evento.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/debugshader"><strong>DebugShader</strong></a></p></td><td><p>Rappresenta informazioni su uno shader nel debugger.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experiment"><strong>Esperimento</strong></a></p></td><td><p>Rappresenta informazioni su un esperimento (acquisizione).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/issue"><strong>Problema</strong></a></p></td><td><p>Rappresenta informazioni su un problema.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/point2d"><strong>Point2D</strong></a></p></td><td><p>Rappresenta un punto 2D con coordinate intere senza segno.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/threaddata3d"><strong>ThreadData3D</strong></a></p></td><td><p>Rappresenta un indice 3D nei dati dei thread</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/inputlayoutstruct"><strong>InputLayoutStruct</strong></a></p></td><td><p>Rappresenta i campi di layout di input di un vertex buffer, uno per ogni campo nel vertex buffer.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryoperation"><strong>PixelHistoryOperation</strong></a></p></td><td><p>Rappresenta informazioni sulla cronologia dei pixel.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryintersection"><strong>PixelHistoryIntersection</strong></a></p></td><td><p>Rappresenta informazioni su un particolare</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/meshdatabufferlayoutentry"><strong>MeshDataBufferLayoutEntry</strong></a></p></td><td><p>Rappresenta informazioni su una singola voce nel layout del buffer di una mesh.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/debugshaderrequestinfo"><strong>DebugShaderRequestInfo</strong></a></p></td><td><p>Rappresenta informazioni su una richiesta del debugger shader.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixengineint4"><strong>PixEngineInt4</strong></a></p></td><td><p>Rappresenta un vettore 4D con coordinate intere con segno.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginepoint4d"><strong>PixEnginePoint4D</strong></a></p></td><td><p>Rappresenta un punto 4D con coordinate a virgola mobile (double) a 64 bit.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginechanneldesc"><strong>PixEngineChannelDesc</strong></a></p></td><td><p>Rappresenta una descrizione di un canale a colori (campione).</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureformatdesc"><strong>PixEngineTextureFormatDesc</strong></a></p></td><td><p>Rappresenta una descrizione di un formato di trama.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturedescriptor"><strong>PixEngineTextureDescriptor</strong></a></p></td><td><p>Rappresenta una descrizione di una risorsa trama.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureslicedescriptor"><strong>PixEngineTextureSliceDescriptor</strong></a></p></td><td><p>Rappresenta una descrizione di una sezione di trama.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturesliceindex"><strong>PixEngineTextureSliceIndex</strong></a></p></td><td><p>Rappresenta l'indice di una sezione di trama</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginehistogram"><strong>PixEngineHistogram</strong></a></p></td><td><p>Rappresenta un istogramma di una trama.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Argomenti correlati

[Informazioni di riferimento su Direct3D Diagnostics Capture Interface](vspixengine-reference.md)

 

 
