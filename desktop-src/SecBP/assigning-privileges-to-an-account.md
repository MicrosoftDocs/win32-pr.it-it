---
description: È possibile assegnare privilegi agli account usando lo snap-in Criteri di sicurezza locali Microsoft Management Console (MMC) (Secpol.msc) o chiamando la funzione LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Assegnazione di privilegi a un account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4ba4fb5266a66aac67b17c70fc6bbcaa1a397a8593534144c688daaee5a0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623011"
---
# <a name="assigning-privileges-to-an-account"></a>Assegnazione di privilegi a un account

È possibile assegnare privilegi agli account usando lo snap-in Criteri di sicurezza locali Microsoft Management Console (MMC) (Secpol.msc) o chiamando la funzione [**LsaAddAccountRights.**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights)

L'assegnazione di un privilegio a un account non influisce sui token utente esistenti. Un utente deve disconnettersi e quindi accedere di nuovo per ottenere un token di accesso con il privilegio appena assegnato.

Per assegnare privilegi tramite lo snap-in MMC Criteri di sicurezza locali, modificare l'elenco di utenti per ogni privilegio elencato in Sicurezza **Impostazioni/Criteri locali/Assegnazione diritti utente**.

 

 
