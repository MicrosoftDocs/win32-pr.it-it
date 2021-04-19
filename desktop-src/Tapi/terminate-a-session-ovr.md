---
description: La chiusura della sessione può avere origine con una richiesta utente, disconnessione remota da parte dell'altra parte o per motivi specifici dell'applicazione.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Terminare una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319851"
---
# <a name="terminate-a-session"></a>Terminare una sessione

La chiusura della sessione può avere origine con una richiesta utente, disconnessione remota da parte dell'altra parte o per motivi specifici dell'applicazione. Quando una sessione viene terminata, l' [identificatore di sessione](session-identifier-ovr.md) rimane valido fino a quando non viene rilasciato in modo specifico e può essere usato per raccogliere i dati di post-connessione.

La chiusura della sessione viene completata deallocando e rilasciando le risorse associate alla sessione. Se una sessione viene semplicemente eliminata o disconnessa, ma le risorse non vengono rilasciate, il risultato è una perdita di memoria nell'applicazione ed eventualmente anche nel provider di servizi.

**TAPI 2. x:** Vedere [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).

**TAPI 3. x:** Vedere [**ITBasicCallControl::D Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), eseguire una versione com standard sul puntatore all'oggetto call.

 

 
