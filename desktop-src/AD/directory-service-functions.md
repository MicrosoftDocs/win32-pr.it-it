---
title: Funzioni del servizio directory (AD DS)
description: Le funzioni del servizio directory forniscono un'utilità per l'individuazione di un controller di dominio (DC) in un dominio Windows NT o Windows 2000.
ms.assetid: 7b519c81-5a6c-470a-a525-1894efd53305
ms.tgt_platform: multiple
keywords:
- Funzioni del servizio directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf37b34c5b1e782bbd297d6a6b5fa81ccfcbc3452e19bf0efc1b7c89ddc530a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018913"
---
# <a name="directory-service-functions-ad-ds"></a>Funzioni del servizio directory (AD DS)

Le funzioni del servizio directory forniscono un'utilità per l'individuazione di un controller di dominio (DC) in un dominio Windows NT o Windows 2000. L'architettura interagisce con i client e i server in tutte le versioni di Windows NT e Windows 2000. Le funzioni seguenti consentono agli sviluppatori di usare il controller di dominio e l'appartenenza al dominio nel servizio directory:

-   [**DsAddressToSiteNames**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesa)
-   [**DsAddressToSiteNamesEx**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesexa)
-   [**DsDeregisterDnsHostRecords**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsderegisterdnshostrecordsa)
-   [**DsEnumerateDomainTrusts**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa)
-   [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)
-   [**Dsgetdcname**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)
-   [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)
-   [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)
-   [**DsGetDcSiteCoverage**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea)
-   [**DsGetForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetforesttrustinformationw)
-   [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea)
-   [**DsMergeForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsmergeforesttrustinformationw)
-   [**DsRoleFreeMemory**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolefreememory)
-   [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation)
-   [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)

Il localizzatore di controller di [**dominio, DsGetDcName,**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)viene implementato dal servizio Netlogon. Ogni controller di dominio registra il proprio nome DNS nel server DNS e il relativo nome NetBIOS usando un meccanismo specifico del trasporto, ad esempio in WINS. Il localizzatore di controller di dominio cerca il nome, quindi invia un datagramma al controller di dominio che ha registrato il nome o effettua il ping. Per i nomi di dominio NetBIOS, il datagramma è un messaggio mailslot. Per i nomi di dominio DNS, il datagramma è una ricerca UDP LDAP. Ogni controller di dominio risponde indicando che è attualmente operativo. Il primo controller di dominio che risponde viene restituito al chiamante.

Il controller di dominio restituito viene memorizzato nella cache, in modo che i chiamanti successivi non devono ripetere l'algoritmo precedente e per incoraggiare tutti i chiamanti a usare lo stesso controller di dominio. Ciò garantisce che un singolo client abbia una visualizzazione coerente del contenuto del controller di dominio.

Quando si cerca un controller di dominio in base al nome di dominio DNS, il localizzatore di controller di dominio tenta di trovare un controller di dominio nel sito "più vicino". Ogni controller di dominio registra record DNS aggiuntivi che indicano il sito in cui si trova il controller di dominio e i siti inclusi nel controller di dominio. Il localizzatore di controller di dominio cerca innanzitutto questo record DNS specifico del sito prima di cercare il record DNS non specifico del sito, preferendo quindi un controller di dominio in tale sito. Quando il localizzatore di controller di dominio invia un datagramma al controller di dominio, il controller di dominio cerca l'indirizzo IP del client nel contenitore Configurazione/Siti/Subnet di DS per trovare un oggetto subnet. La **proprietà siteObject** dell'oggetto subnet definisce il nome del sito che contiene il client. Il controller di dominio risponde al ping con il nome del sito che contiene il client, insieme a un indicatore che indica se il controller di dominio copre tale sito. Se il controller di dominio non include tale sito e il localizzatore di controller di dominio non ha ancora tentato di trovare un controller di dominio in tale sito, il localizzatore di controller di dominio tenta di nuovo di trovare un controller di dominio nel sito.

Per trovare il nome del sito contenente il client, usare la [**funzione DsGetSiteName.**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) I nomi degli oggetti nel contenitore Configuration/Sites/Subnet devono essere nomi di subnet validi. La [**funzione DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea) indica se un nome di subnet specificato è valido.

 

 




