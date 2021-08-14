---
description: Per determinare se un descrittore di sicurezza è relativo o assoluto, chiamare la funzione GetSecurityDescriptorControl e controllare il flag edizione Standard SELF RELATIVE del parametro \_ \_ SECURITY \_ DESCRIPTOR \_ CONTROL.
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Descrittori di sicurezza assoluti e Self-Relative di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a2639d1f17527b92116eabcaca96b637012253bbafc42198e37c9867fc585c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914723"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Descrittori di sicurezza assoluti e Self-Relative di sicurezza

Un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) può essere in [*formato*](/windows/desktop/SecGloss/a-gly) assoluto [*o auto-relativo.*](/windows/desktop/SecGloss/s-gly) In formato assoluto, un descrittore di sicurezza contiene puntatori alle relative informazioni, non alle informazioni. In formato auto-relativo, un descrittore di sicurezza archivia una [**struttura SECURITY \_ DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e le informazioni di sicurezza associate in un blocco contiguo di memoria. Per determinare se un descrittore di sicurezza è relativo o assoluto, chiamare la funzione [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) e controllare il flag edizione Standard SELF RELATIVE del parametro \_ \_ SECURITY [**\_ DESCRIPTOR \_ CONTROL.**](security-descriptor-control.md) È possibile usare le [**funzioni MakeSelfRelativeSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) e [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) per la conversione tra questi due formati.

Il formato assoluto è utile quando si compila un descrittore di sicurezza e si hanno puntatori a tutti i componenti, ad esempio quando sono disponibili le impostazioni predefinite per il proprietario, il gruppo e l'ACL discrezionale. In questo caso, è possibile chiamare la funzione [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) per inizializzare una struttura [**SECURITY \_ DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e quindi chiamare funzioni come [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) per assegnare puntatori ACL e SID al descrittore di sicurezza.

Nel formato auto-relativo, un descrittore di sicurezza inizia sempre con una struttura [**SECURITY \_ DESCRIPTOR,**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) ma gli altri componenti del descrittore di sicurezza possono seguire la struttura in qualsiasi ordine. Invece di usare gli indirizzi di memoria, i componenti del descrittore di sicurezza sono identificati dagli offset dall'inizio del descrittore. Questo formato è utile quando un descrittore di sicurezza deve essere archiviato su disco, trasmesso tramite un protocollo di comunicazione o copiato in memoria.

Ad eccezione [**di MakeAbsoluteSD,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd)tutte le funzioni che restituiscono un descrittore di sicurezza usano il formato auto-relativo. I descrittori di sicurezza passati come argomenti a una funzione possono essere di tipo auto-relativo o assoluto. Per altre informazioni, vedere la documentazione relativa alla funzione .

 

 
