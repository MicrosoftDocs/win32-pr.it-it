---
description: I buffer specifici del dispositivo possono far parte di un'implementazione dei provider di servizi di operazioni estese. Il provider di servizi definisce il significato di questi buffer.
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: Buffer specifico del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311906"
---
# <a name="device-specific-buffer"></a>Buffer specifico del dispositivo

I buffer specifici del dispositivo possono far parte dell'implementazione di un provider di servizi di operazioni estese. Il provider di servizi definisce il significato di questi buffer.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwDevSpecificSize** and **dwDevSpecificOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3. x:** Vedere [**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (membro **CIB \_ DEVSPECIFICBUFFER** del [**\_ buffer CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
