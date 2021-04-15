---
title: Sicurezza attivazione
description: Sicurezza attivazione
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474406"
---
# <a name="activation-security"></a>Sicurezza attivazione

La sicurezza per l'attivazione (detta anche sicurezza di avvio) consente di controllare gli utenti che possono avviare un server. La sicurezza per l'attivazione viene applicata automaticamente da Gestione controllo servizi (SCM) di un determinato computer. Al momento della ricezione di una richiesta da parte di un client per l'attivazione di un oggetto (come descritto in [funzioni helper](instance-creation-helper-functions.md)per la creazione di istanze), SCM controlla la richiesta rispetto alle informazioni di sicurezza di attivazione archiviate nel registro di sistema. La sicurezza dell'attivazione viene verificata anche per le attivazioni dello stesso computer.

Quando si determina l'identità del client, l'attivazione esamina il flag di mascheramento impostato nella chiamata del client a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Se viene impostato il flag di mascheramento (per mascheramento statico o dinamico), viene utilizzato il token del thread, se presente, per determinare l'identità del client. Se non è impostato alcun mascheramento, viene utilizzato il token di processo anziché il token del thread.

Per ulteriori informazioni sulla sicurezza dell'attivazione, vedere [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) e [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 