---
description: Callback per restituire l'elenco di eventi in un frame.
MS-HAID: vspixengine.IFrameEventsCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IFrameEventsCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F40DD5DC-E78E-41F3-9D25-4D7CAE27DE45
api_name:
- IFrameEventsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 98815681db182c99a86c05c1ea22eaad41526438
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304031"
---
# <a name="span-idvspixengineiframeeventscallbackspaniframeeventscallback-interface"></a><span id="vspixengine.iframeeventscallback"></span>Interfaccia IFrameEventsCallback

Callback per restituire l'elenco di eventi in un frame.

## <a name="members"></a>Membri

L'interfaccia **IFrameEventsCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IFrameEventsCallback** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

L'interfaccia **IFrameEventsCallback** dispone di questi metodi.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></td><td style="text-align: left;"><p>Ottiene informazioni sulle colonne (tipi di dati dell'evento) supportate dall'elenco di eventi.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></td><td style="text-align: left;"><p>Funzione di callback utilizzata per notificare all'host le informazioni sugli eventi nell'elenco degli eventi.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
