---
description: Callback per restituire le versioni di tutte le interfacce supportate. Ciò consente al consumer di non essere sincronizzato con il motore di acquisizione.
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
ms.openlocfilehash: 905c6f085695ba20b7cdd3a363c3af5a833d598a
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787487"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span id="vspixengine.iversioncallback"></span>Interfaccia IVersionCallback

Callback per restituire le versioni di tutte le interfacce supportate. Ciò consente al consumer di non essere sincronizzato con il motore di acquisizione.

## <a name="members"></a>Membri

**L'interfaccia IVersionCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IVersionCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

**L'interfaccia IVersionCallback** include questi metodi.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Metodo</th><th >Descrizione</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></td><td ><p>Funzione di callback utilizzata per notificare all'host le interfacce supportate.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
