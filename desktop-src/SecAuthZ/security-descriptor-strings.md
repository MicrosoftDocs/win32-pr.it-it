---
description: Un descrittore di sicurezza funzionale valido contiene informazioni di sicurezza in formato binario.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Stringhe del descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbefeb87a7fca30f0c33d6f180315df5e5d576dc018e69dc680391050a840d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413791"
---
# <a name="security-descriptor-strings"></a>Stringhe del descrittore di sicurezza

Un descrittore di [*sicurezza funzionale valido*](/windows/desktop/SecGloss/s-gly) contiene informazioni di sicurezza in formato binario. L Windows API fornisce funzioni per la conversione di descrittori di sicurezza binari da e verso stringhe di testo. I descrittori di sicurezza in formato stringa non sono funzionali, ma possono essere utili per l'archiviazione o il trasporto di informazioni sui descrittori di sicurezza.

Per convertire un descrittore di sicurezza in un formato stringa, chiamare la [**funzione ConvertSecurityDescriptorToStringSecurityDescriptor.**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) Per convertire un descrittore di sicurezza in formato stringa in un descrittore di sicurezza funzionale valido, chiamare la [**funzione ConvertStringSecurityDescriptorToSecurityDescriptor.**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Per altre informazioni, vedere [Linguaggio di definizione del descrittore di sicurezza](security-descriptor-definition-language.md).

 

 
