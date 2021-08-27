---
description: Quando si crea un pacchetto di sicurezza SSP (Security Support Provider), non è consigliabile consentire al client aggiunto al dominio di eseguire l'autenticazione a un controller di dominio usando un nome SPN (Service Provider Name) in due parti nel formato seguente.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Uso dei nomi delle entità in tre parti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ddc9ce552e71d97c5e795b7405e97803991133a96e7b3fac3e1a81bc45d5ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915184"
---
# <a name="using-three-part-principal-names"></a>Uso dei nomi delle entità in tre parti

Quando si crea un pacchetto di sicurezza SSP (Security Support Provider), non è consigliabile consentire al client aggiunto al dominio di eseguire l'autenticazione a un controller di dominio usando un nome SPN (Service Provider Name) in due parti nel formato seguente.

-   <*protocollo* >/< *nome host*>

Un client deve sempre eseguire l'autenticazione specificando il dominio.

-   <*protocollo* >/< *nome host* >/< *nome di dominio*>

Un client aggiunto a un dominio che accede con un nome SPN in due parti può essere in grado di rappresentare il controller di dominio. Se si consentono nomi SPN in due parti, è necessario creare una voce di log contenente informazioni sufficienti per consentire all'amministratore di identificare il chiamante.

 

 



