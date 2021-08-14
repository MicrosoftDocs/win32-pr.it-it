---
description: Callback per restituire le istruzioni generate dalla creazione di una traccia dello shader.
MS-HAID: vspixengine.IDebugShaderCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IDebugShaderCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A4A3FD3-15E5-4DB5-8777-55797E32ABA3
api_name:
- IDebugShaderCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf11c453ccf1d9431e5273ec909015de5916ff3faccc0c3d06d1cb8d29073870
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981581"
---
# <a name="span-idvspixengineidebugshadercallbackspanidebugshadercallback-interface"></a><span id="vspixengine.idebugshadercallback"></span>Interfaccia IDebugShaderCallback

Callback per restituire le istruzioni generate dalla creazione di una traccia dello shader.

## <a name="members"></a>Membri

**L'interfaccia IDebugShaderCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDebugShaderCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Metodi

**L'interfaccia IDebugShaderCallback** include questi metodi.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Metodo</th><th style="text-align: left;">Descrizione</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></td><td style="text-align: left;"><p>Callback che notifica all'host le informazioni di istruzioni restituite dalla richiesta associata.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
