---
title: Funzioni del servizio directory (AD DS)
description: Le funzioni del servizio directory forniscono un'utilità per l'individuazione di un controller di dominio in un dominio Windows NT o Windows 2000.
ms.assetid: 7b519c81-5a6c-470a-a525-1894efd53305
ms.tgt_platform: multiple
keywords:
- Funzioni del servizio directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b071128806926e07cf61d62e53b823d8e7e1ac
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "104046199"
---
# <a name="directory-service-functions-ad-ds"></a>Funzioni del servizio directory (AD DS)

Le funzioni del servizio directory forniscono un'utilità per l'individuazione di un controller di dominio in un dominio Windows NT o Windows 2000. L'architettura interagisce con i client e i server in tutte le versioni di Windows NT e Windows 2000. Le funzioni seguenti consentono agli sviluppatori di utilizzare il controller di dominio e l'appartenenza al dominio nel servizio directory:

-   [**DsAddressToSiteNames**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesa)
-   [**DsAddressToSiteNamesEx**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesexa)
-   [**DsDeregisterDnsHostRecords**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsderegisterdnshostrecordsa)
-   [**DsEnumerateDomainTrusts**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa)
-   [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)
-   [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)
-   [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)
-   [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)
-   [**DsGetDcSiteCoverage**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea)
-   [**DsGetForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetforesttrustinformationw)
-   [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea)
-   [**DsMergeForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsmergeforesttrustinformationw)
-   [**DsRoleFreeMemory**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolefreememory)
-   [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation)
-   [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)

Il localizzatore del controller di dominio, [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea), viene implementato dal servizio Netlogon. Ogni controller di dominio registra il nome DNS nel server DNS e il relativo nome NetBIOS usando un meccanismo specifico del trasporto, ad esempio in WINS. Il localizzatore del controller di dominio cerca il nome, quindi Invia un datagramma a, o ping, il controller di dominio che ha registrato il nome. Per i nomi di dominio NetBIOS, il datagramma è un messaggio inserimento/espulsione. Per i nomi di dominio DNS, il datagramma è una ricerca UDP LDAP. Ogni controller di dominio di questo tipo risponde indicando che è attualmente operativo. Il primo controller di dominio da rispondere viene restituito al chiamante.

Il controller di dominio restituito viene memorizzato nella cache, in modo che i chiamanti successivi non debbano ripetere l'algoritmo precedente e incoraggiare tutti i chiamanti a usare lo stesso controller di dominio. In questo modo si garantisce che un singolo client disponga di una visualizzazione coerente del contenuto del controller di dominio.

Quando si cerca un controller di dominio in base al nome di dominio DNS, DC Locator tenta di trovare un controller di dominio nel sito "più vicino". Ogni controller di dominio registra record DNS aggiuntivi che indicano il sito in cui si trova il controller di dominio e i siti inclusi nel controller di dominio. DC Locator cerca innanzitutto questo record DNS specifico del sito prima di cercare il record DNS che non è specifico del sito, in modo che preferisca un controller di dominio in tale sito. Quando il localizzatore del controller di dominio invia un datagramma al controller di dominio, il controller di dominio cerca l'indirizzo IP del client nel contenitore di configurazione/siti/subnet del DS per trovare un oggetto subnet. La proprietà **siteObject** dell'oggetto subnet definisce il nome del sito che contiene il client. Il controller di dominio risponde al ping con il nome del sito che contiene il client, insieme a un indicatore che indica se il controller di dominio copre tale sito. Se il controller di dominio non include il sito e il localizzatore del controller di dominio non ha ancora tentato di trovare un controller di dominio in tale sito, il localizzatore controller di dominio tenterà nuovamente di trovare un controller di dominio nel sito.

Per trovare il nome del sito contenente il client, usare la funzione [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) . I nomi degli oggetti nel contenitore Configuration/sites/subnet devono essere nomi di subnet validi. La funzione [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea) indica se il nome di una subnet specificato è valido.

 

 




