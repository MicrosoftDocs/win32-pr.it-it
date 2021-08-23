---
description: Il privilegio indica se un'applicazione è proprietaria o sta monitorando la sessione.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilege
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4423b5eb1d50f5a7329726ab2e01040971daecca7e603247c49bcbc1d7c6d570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060579"
---
# <a name="privilege"></a>Privilege

Il privilegio indica se un'applicazione è proprietaria o sta monitorando la sessione. Se l'applicazione è proprietaria della sessione, è possibile eseguire un'ampia gamma di operazioni di sessione. Se l'applicazione esegue solo il monitoraggio, riceverà messaggi di stato e potrà accedere alle informazioni sulla sessione, ma qualsiasi tentativo di eseguire la maggior parte delle operazioni restituirà un errore.

Durante l'inizializzazione, un'applicazione indica a TAPI il livello di privilegio richiesto per gli indirizzi. TAPI offre sessioni in ingresso solo alle applicazioni registrate per il proprietario o il proprietario e il privilegio di monitoraggio.

Il privilegio di un'applicazione in una sessione creata è sempre proprietario.

**TAPI 2.x:** Vedere [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** membro di [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**TAPI 3.x:** Vedere [**ITCallInfo::get \_ Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chiamato con il membro **CIL \_ NUMBEROFOWNERS** o **CIL \_ NUMBEROFMONITORS** di [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
