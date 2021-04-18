---
description: È possibile assegnare privilegi agli account tramite lo snap-in criteri di sicurezza locali (secpol. msc) o chiamando la funzione LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Assegnazione di privilegi a un account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315423"
---
# <a name="assigning-privileges-to-an-account"></a>Assegnazione di privilegi a un account

È possibile assegnare privilegi agli account tramite lo snap-in criteri di sicurezza locali (secpol. msc) o chiamando la funzione [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) .

L'assegnazione di un privilegio a un account non influisce sui token utente esistenti. Un utente deve disconnettersi e quindi eseguire di nuovo l'accesso per ottenere un token di accesso con il privilegio appena assegnato.

Per assegnare privilegi tramite lo snap-in MMC Criteri di sicurezza locali, modificare l'elenco di utenti per ogni privilegio elencato in **impostazioni di sicurezza/Criteri locali/Assegnazione diritti utente**.

 

 
