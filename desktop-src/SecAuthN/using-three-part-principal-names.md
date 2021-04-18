---
description: Quando si crea un pacchetto di sicurezza di Security Support Provider (SSP), è consigliabile non consentire al client aggiunto al dominio di eseguire l'autenticazione a un controller di dominio utilizzando un nome del provider di servizi (SPN) in due parti nel formato seguente.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Uso di tre nomi di entità parte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306548"
---
# <a name="using-three-part-principal-names"></a>Uso di tre nomi di entità parte

Quando si crea un pacchetto di sicurezza di Security Support Provider (SSP), è consigliabile non consentire al client aggiunto al dominio di eseguire l'autenticazione a un controller di dominio utilizzando un nome del provider di servizi (SPN) in due parti nel formato seguente.

-   <*protocollo* >/< di *nome host*>

Un client deve sempre eseguire l'autenticazione specificando il dominio.

-   <*protocollo* >/< di *nome host* >/< *nome di dominio*>

Un client aggiunto a un dominio che esegue l'accesso con un SPN a due parti potrebbe essere in grado di rappresentare il controller di dominio. Se si concedono due SPN della parte, è necessario creare una voce di log contenente informazioni sufficienti per consentire all'amministratore di identificare il chiamante.

 

 



