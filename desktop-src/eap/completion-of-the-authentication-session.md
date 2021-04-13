---
title: Completamento della sessione di autenticazione
description: Al termine della sessione di autenticazione, il servizio di autenticazione chiama la funzione RasEapEnd per consentire al protocollo di autenticazione di deallocare il buffer di lavoro.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27899ef348630e412b3d52d066f59ea9b5255244
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398915"
---
# <a name="completion-of-the-authentication-session"></a>Completamento della sessione di autenticazione

Al termine della sessione di autenticazione, il servizio di autenticazione chiama la funzione [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) per consentire al protocollo di autenticazione di deallocare il buffer di lavoro. Questa azione viene eseguita indipendentemente dal fatto che l'autenticazione abbia avuto esito positivo. La chiamata della funzione **RasEapEnd** garantisce che non vengano effettuate ulteriori chiamate al protocollo di autenticazione utilizzando quel particolare utente o contesto senza prima chiamare [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

 

 