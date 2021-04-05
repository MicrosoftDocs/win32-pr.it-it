---
description: Per determinare se un descrittore di sicurezza è autonomo o assoluto, chiamare la funzione GetSecurityDescriptorControl e controllare \_ il \_ flag se self relativa del \_ parametro di controllo del descrittore di sicurezza \_ .
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Descrittori di sicurezza assoluti e Self-Relative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57406e194a31e79594394913055609e2981e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967715"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Descrittori di sicurezza assoluti e Self-Relative

Un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) può essere in formato [*assoluto*](/windows/desktop/SecGloss/a-gly) o [*relativo*](/windows/desktop/SecGloss/s-gly) . In un formato assoluto, un descrittore di sicurezza contiene i puntatori alle relative informazioni e non le informazioni. Nel formato relativo, un descrittore di sicurezza archivia una struttura del [**\_ descrittore di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e le informazioni di sicurezza associate in un blocco di memoria contiguo. Per determinare se un descrittore di sicurezza è autonomo o assoluto, chiamare la funzione [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) e controllare il \_ flag se self \_ relativa del parametro di [**\_ \_ controllo del descrittore di sicurezza**](security-descriptor-control.md) . È possibile utilizzare le funzioni [**presunto MakeSelfRelativeSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) e [**presunto MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) per la conversione tra questi due formati.

Il formato assoluto è utile quando si compila un descrittore di sicurezza e si hanno puntatori a tutti i componenti, ad esempio quando sono disponibili le impostazioni predefinite per il proprietario, il gruppo e l'ACL discrezionale. In questo caso, è possibile chiamare la funzione [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) per inizializzare una struttura del [**\_ descrittore di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e quindi chiamare funzioni quali [**SETSECURITYDESCRIPTORDACL**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) per assegnare i puntatori ACL e SID al descrittore di sicurezza.

Nel formato relativo, un descrittore di sicurezza inizia sempre con una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , ma gli altri componenti del descrittore di sicurezza possono seguire la struttura in qualsiasi ordine. Anziché utilizzare gli indirizzi di memoria, i componenti del descrittore di sicurezza sono identificati da offset dall'inizio del descrittore. Questo formato è utile quando un descrittore di sicurezza deve essere archiviato su disco, trasmesso tramite un protocollo di comunicazione o copiato in memoria.

Ad eccezione di [**presunto MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd), tutte le funzioni che restituiscono un descrittore di sicurezza lo eseguono utilizzando il formato relativo. I descrittori di sicurezza passati come argomenti a una funzione possono essere di tipo autonomo o assoluto. Per ulteriori informazioni, vedere la documentazione relativa alla funzione.

 

 
