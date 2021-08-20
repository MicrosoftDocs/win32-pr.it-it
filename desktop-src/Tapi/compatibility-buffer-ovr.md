---
description: Il buffer di compatibilità è specifico dello standard ISDN Q.931. Fare riferimento alla documentazione dei provider di servizi sul significato e sull'uso di questi dati.
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: Buffer di compatibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739063a6570a93b1fb05442ebe3f6ec10a040626ba7a0fe4b9692d7e5636b5ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946593"
---
# <a name="compatibility-buffer"></a>Buffer di compatibilità

Il buffer di compatibilità è specifico dello standard ISDN Q.931. Fare riferimento alla documentazione del provider di servizi sul significato e sull'uso di questi dati.

Non tutti i provider di servizi supportano l'uso di queste informazioni.

**TAPI 2.x:** Vedere i membri [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize** e **dwLowLevelCompOffset** *di lpCallInfo*).

**TAPI 3.x:** Vedere [**ITCallInfo::get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ HIGHLEVELCOMPATIBILITYBUFFER** e **MEMBRO CIB \_ LOWLEVELCOMPATIBILITYBUFFER** di [**CALLINFO \_ BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
