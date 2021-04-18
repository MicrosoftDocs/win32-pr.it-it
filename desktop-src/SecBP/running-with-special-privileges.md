---
description: Alcune funzioni richiedono privilegi speciali per una corretta esecuzione.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Esecuzione con privilegi speciali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318248"
---
# <a name="running-with-special-privileges"></a>Esecuzione con privilegi speciali

Alcune funzioni richiedono [privilegi](/windows/desktop/SecAuthZ/privileges) speciali per una corretta esecuzione. In alcuni casi, la funzione può essere eseguita solo da determinati utenti o da membri di determinati gruppi. Il requisito più comune è che l'utente sia un amministratore locale. Per altre funzioni è necessario che l'account dell'utente disponga di privilegi specifici abilitati.

Per ridurre la possibilità che il codice non autorizzato possa ottenere il controllo, il sistema deve essere eseguito con il privilegio minimo necessario. Le applicazioni che devono chiamare funzioni che richiedono privilegi speciali possono lasciare il sistema aperto per attaccare gli hacker. Tali applicazioni devono essere progettate per essere eseguite per brevi periodi di tempo e informare l'utente delle implicazioni di sicurezza implicate.

Per informazioni sull'esecuzione di come utenti diversi e su come abilitare i privilegi nell'applicazione, vedere gli argomenti seguenti:<dl>

[Esecuzione con privilegi di amministratore](running-with-administrator-privileges.md)  
[Chiedere all'utente le credenziali](asking-the-user-for-credentials.md)  
[Modifica dei privilegi in un token](changing-privileges-in-a-token.md)  
[Assegnazione di privilegi a un account](assigning-privileges-to-an-account.md)  
</dl>

 

 
