---
description: Microsoft ha introdotto l'interfaccia DPAPI (Data Protection Application Programming Interface) Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: CNG DPAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0273522580c806caa5fe7848ff32a2017cfb37c4499dee21f5a3787ecae57b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908630"
---
# <a name="cng-dpapi"></a>CNG DPAPI

Microsoft ha introdotto l'interfaccia DPAPI (Data Protection Application Programming Interface) Windows 2000. L'API è costituita da due funzioni, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) DPAPI fa parte di CryptoAPI ed è stato progettato per gli sviluppatori che non erano a loro affezionati all'uso della crittografia. Le due funzioni possono essere usate per crittografare e decrittografare i dati statici in un singolo computer.

Il cloud computing, tuttavia, spesso richiede che il contenuto crittografato in un computer sia decrittografato in un altro. Pertanto, a partire da Windows 8, Microsoft ha esteso l'idea di usare un'API relativamente semplice per includere scenari cloud. Questa nuova API, denominata DPAPI-NG, consente di condividere in modo sicuro segreti (chiavi, password, materiale della chiave) e messaggi proteggendoli in un set di entità che possono essere usate per rimuovere la protezione in computer diversi dopo l'autenticazione e l'autorizzazione appropriate. Le entità di sicurezza seguenti sono attualmente supportate:

-   Gruppo in una foresta Active Directory.
-   Credenziali Web.

Per altre informazioni, vedere i seguenti argomenti:

-   [Provider di protezione](protection-providers.md)
-   [Descrittori di protezione](protection-descriptors.md)
-   [Formato dati protetti](protected-data-format.md)

DPAPI-NG è basato su Cryptography Next Generation (CNG) e include le funzioni seguenti:

-   [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [**NCryptCloseProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [**NCryptProtectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [**NCryptQueryProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [**NCryptStreamClose**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [**NCryptStreamOpenToProtect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [**NCryptStreamOpenToUnprotect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [**NCryptStreamUpdate**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [**NCryptUnprotectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
