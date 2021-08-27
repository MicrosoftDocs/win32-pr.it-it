---
title: Sicurezza dell'attivazione
description: Sicurezza dell'attivazione
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be436997889edd14704d5fa7646db689bba405825c1e8bcf9d021ea850ae70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048909"
---
# <a name="activation-security"></a>Sicurezza dell'attivazione

La sicurezza dell'attivazione (detta anche sicurezza di avvio) consente di controllare chi può avviare un server. La sicurezza dell'attivazione viene applicata automaticamente dal gestore di controllo del servizio (SCM) di un computer specifico. Dopo la ricezione di una richiesta da parte di un client per attivare un oggetto (come descritto [in](instance-creation-helper-functions.md)Funzioni helper per la creazione di istanze), Gestione controllo servizi controlla la richiesta rispetto alle informazioni di sicurezza di attivazione archiviate nel registro. La sicurezza dell'attivazione viene verificata anche per le attivazioni dello stesso computer.

Quando si determina l'identità del client, l'attivazione esamina il flag di cloaking impostato nella chiamata del client a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Se il flag di cloaking è impostato (per cloaking dinamico o statico), il token del thread viene usato, se presente, per determinare l'identità del client. Se non è impostato alcun cloaking, viene usato il token di processo anziché il token del thread.

Per altre informazioni sulla sicurezza dell'attivazione, vedere [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) e [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 