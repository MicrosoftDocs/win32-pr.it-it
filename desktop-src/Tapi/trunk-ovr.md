---
description: Numero del trunk su cui viene instradata la chiamata. Questo membro viene usato sia per le chiamate in ingresso che per le chiamate in uscita.
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: Trunk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676721df074d0fe84efbe3256da3e111e94932e0b99d5614d792ddbb0c860ca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872561"
---
# <a name="trunk"></a>Trunk

Numero del trunk su cui viene instradata la chiamata. Questo membro viene usato sia per le chiamate in ingresso che per le chiamate in uscita.

Non tutti i provider di servizi supportano l'uso di queste informazioni.

**TAPI 2.x: **[**lineGetCallInfo,**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) **dwTrunk** di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chiamato con il membro **\_ CIL TRUNK** di [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
