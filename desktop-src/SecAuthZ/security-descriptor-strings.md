---
description: Un descrittore di sicurezza funzionale valido contiene informazioni sulla sicurezza in formato binario.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Stringhe del descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb875bee4d35267b578193ca7cd08420722400a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129902"
---
# <a name="security-descriptor-strings"></a>Stringhe del descrittore di sicurezza

Un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) funzionale valido contiene informazioni sulla sicurezza in formato binario. L'API Windows fornisce funzioni per la conversione di descrittori di sicurezza binari da e verso stringhe di testo. I descrittori di sicurezza in formato stringa non sono funzionali, ma possono essere utili per archiviare o trasferire informazioni sul descrittore di sicurezza.

Per convertire un descrittore di sicurezza in un formato stringa, chiamare la funzione [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) . Per convertire di nuovo un descrittore di sicurezza in formato stringa in un descrittore di sicurezza funzionale valido, chiamare la funzione [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .

Per ulteriori informazioni, vedere [Security Descriptor Definition Language](security-descriptor-definition-language.md).

 

 
