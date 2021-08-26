---
title: Completamento della sessione di autenticazione
description: Al termine della sessione di autenticazione, il servizio di autenticazione chiama la funzione RasEapEnd per consentire al protocollo di autenticazione di deallocare il buffer di lavoro.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee29ac4c4139fc8a575e7570e3c04fbe449aa4d619cea3e096cd12dfcf19bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948471"
---
# <a name="completion-of-the-authentication-session"></a>Completamento della sessione di autenticazione

Al termine della sessione di autenticazione, il servizio di autenticazione chiama la [**funzione RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) per consentire al protocollo di autenticazione di deallocare il buffer di lavoro. Questa azione viene eseguita indipendentemente dal fatto che l'autenticazione sia stata eseguita correttamente. La chiamata **alla funzione RasEapEnd** garantisce che non vengono effettuate altre chiamate al protocollo di autenticazione usando tale utente o contesto specifico senza prima chiamare [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

 

 