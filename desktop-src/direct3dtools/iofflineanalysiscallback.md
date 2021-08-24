---
description: Callback a che restituisce dati di analisi offline.
MS-HAID: vspixengine.IOfflineAnalysisCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IOfflineAnalysisCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 39E6B9CA-C17A-42C8-AC6D-118DC8DE3AD9
api_name:
- IOfflineAnalysisCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09f1a2d2d4be258cc7288f4bced9262ba53daaeda013429a72a0006e27ae6665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853211"
---
# <a name="span-idvspixengineiofflineanalysiscallbackspaniofflineanalysiscallback-interface"></a><span id="vspixengine.iofflineanalysiscallback"></span>Interfaccia IOfflineAnalysisCallback

Callback a che restituisce dati di analisi offline.

## <a name="members"></a>Membri

**L'interfaccia IOfflineAnalysisCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IOfflineAnalysisCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

**L'interfaccia IOfflineAnalysisCallback** include questi metodi.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></td><td style="text-align: left;"><p>Funzione di callback utilizzata per notificare all'host che l'analisi offline è stata completata.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></td><td style="text-align: left;"><p>Funzione di callback utilizzata per notificare all'host lo stato di avanzamento dell'analisi offline.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
