---
description: Callback per restituire le versioni di tutte le interfacce supportate. In questo modo il consumer non è sincronizzato con il motore di acquisizione.
MS-HAID: vspixengine.IVersionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IVersionCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7135E175-C537-4B0C-8F0A-CB77E3F2D945
api_name:
- IVersionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c3ff23d325ff7b9d2783c9e35ca523253cea2880453c46f94a7d915cb47e8f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119415"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span id="vspixengine.iversioncallback"></span>Interfaccia IVersionCallback

Callback per restituire le versioni di tutte le interfacce supportate. In questo modo il consumer non è sincronizzato con il motore di acquisizione.

## <a name="members"></a>Membri

**L'interfaccia IVersionCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IVersionCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

**L'interfaccia IVersionCallback** include questi metodi.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></td><td style="text-align: left;"><p>Funzione di callback utilizzata per notificare all'host quali interfacce sono supportate.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
