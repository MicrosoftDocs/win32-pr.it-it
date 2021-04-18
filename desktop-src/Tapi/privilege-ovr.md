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
# <a name="privilege"></a><span data-ttu-id="c9c82-103">Privilege</span><span class="sxs-lookup"><span data-stu-id="c9c82-103">Privilege</span></span>

<span data-ttu-id="c9c82-104">Il privilegio indica se un'applicazione è di proprietà o sta monitorando la sessione.</span><span class="sxs-lookup"><span data-stu-id="c9c82-104">Privilege refers to whether an application owns or is monitoring the session.</span></span> <span data-ttu-id="c9c82-105">Se l'applicazione è proprietaria della sessione, è consentita l'esecuzione di una serie di operazioni di sessione.</span><span class="sxs-lookup"><span data-stu-id="c9c82-105">If the application owns the session, it is allowed to perform a variety of session operations.</span></span> <span data-ttu-id="c9c82-106">Se l'applicazione è solo Monitoring, riceverà messaggi di stato e potrà accedere alle informazioni sulla sessione, ma qualsiasi tentativo di eseguire la maggior parte delle operazioni genererà un errore.</span><span class="sxs-lookup"><span data-stu-id="c9c82-106">If the application is only monitoring, it will receive state messages and it can access session information, but any attempt to perform most operations will result in an error.</span></span>

<span data-ttu-id="c9c82-107">Durante l'inizializzazione, un'applicazione indica a TAPI il livello di privilegio necessario per gli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="c9c82-107">During initialization, an application tells TAPI which privilege level it requires on which addresses.</span></span> <span data-ttu-id="c9c82-108">TAPI offre sessioni in entrata solo per le applicazioni che sono state registrate per il proprietario o il proprietario e il privilegio di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="c9c82-108">TAPI offers incoming sessions only to applications that have registered for either owner or owner and monitor privilege.</span></span>

<span data-ttu-id="c9c82-109">Il privilegio di un'applicazione in una sessione creata è sempre proprietario.</span><span class="sxs-lookup"><span data-stu-id="c9c82-109">An application's privilege on a session it creates is always owner.</span></span>

<span data-ttu-id="c9c82-110">**TAPI 2. x:** Vedere [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), membro **dwCallPrivilege** di [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span><span class="sxs-lookup"><span data-stu-id="c9c82-110">**TAPI 2.x:** See [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span></span>

<span data-ttu-id="c9c82-111">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chiamato con il membro **CIL \_ NUMBEROFOWNERS** o **CIL \_ NUMBEROFMONITORS** di [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="c9c82-111">**TAPI 3.x:** See [**ITCallInfo::get\_Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_NUMBEROFOWNERS** or **CIL\_NUMBEROFMONITORS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
