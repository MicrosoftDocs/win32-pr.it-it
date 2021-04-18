---
description: Il buffer di compatibilità è specifico dello standard ISDN Q. 931. Per informazioni sul significato e sull'uso di questi dati, fare riferimento alla documentazione del provider di servizi.
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: Buffer di compatibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8669e32cd47978c10e2f5abdbe076bcf08ba1862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308311"
---
# <a name="compatibility-buffer"></a>Buffer di compatibilità

Il buffer di compatibilità è specifico dello standard ISDN Q. 931. Per informazioni sul significato e sull'uso di questi dati, vedere la documentazione del provider di servizi.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize** e **dwLowLevelCompOffset** membri di *lpCallInfo*).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ HIGHLEVELCOMPATIBILITYBUFFER** e **CIB \_** LOWLEVELCOMPATIBILITYBUFFER member of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
