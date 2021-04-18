---
description: Microsoft ha introdotto Data Protection Application Programming Interface (DPAPI) in Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: DPAPI CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305851"
---
# <a name="cng-dpapi"></a>DPAPI CNG

Microsoft ha introdotto Data Protection Application Programming Interface (DPAPI) in Windows 2000. L'API è costituita da due funzioni, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata). DPAPI è parte di CryptoAPI ed è destinato agli sviluppatori che conoscevano molto poco l'uso della crittografia. Le due funzioni possono essere utilizzate per crittografare e decrittografare i dati statici in un singolo computer.

Il cloud computing, tuttavia, richiede spesso che il contenuto crittografato in un computer venga decrittografato in un altro computer. Pertanto, a partire da Windows 8, Microsoft ha esteso l'idea di usare un'API relativamente semplice per includere scenari cloud. Questa nuova API, denominata DPAPI-NG, consente di condividere in modo sicuro i segreti (chiavi, password, materiale della chiave) e i messaggi protetti in un set di entità che possono essere usate per rimuovere la protezione in computer diversi dopo l'autenticazione e l'autorizzazione corrette. Attualmente sono supportate le entità seguenti:

-   Gruppo in una foresta Active Directory.
-   Credenziali Web.

Per altre informazioni, vedere i seguenti argomenti:

-   [Provider di protezione](protection-providers.md)
-   [Descrittori di protezione](protection-descriptors.md)
-   [Formato dati protetto](protected-data-format.md)

DPAPI-NG si basa su Cryptography Next Generation (CNG) e include le funzioni seguenti:

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

 

 
