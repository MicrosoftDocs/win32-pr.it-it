---
description: Il privilegio indica se un'applicazione è di proprietà o sta monitorando la sessione.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilege
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316037"
---
# <a name="privilege"></a>Privilege

Il privilegio indica se un'applicazione è di proprietà o sta monitorando la sessione. Se l'applicazione è proprietaria della sessione, è consentita l'esecuzione di una serie di operazioni di sessione. Se l'applicazione è solo Monitoring, riceverà messaggi di stato e potrà accedere alle informazioni sulla sessione, ma qualsiasi tentativo di eseguire la maggior parte delle operazioni genererà un errore.

Durante l'inizializzazione, un'applicazione indica a TAPI il livello di privilegio necessario per gli indirizzi. TAPI offre sessioni in entrata solo per le applicazioni che sono state registrate per il proprietario o il proprietario e il privilegio di monitoraggio.

Il privilegio di un'applicazione in una sessione creata è sempre proprietario.

**TAPI 2. x:** Vedere [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), membro **dwCallPrivilege** di [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chiamato con il membro **CIL \_ NUMBEROFOWNERS** o **CIL \_ NUMBEROFMONITORS** di [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
