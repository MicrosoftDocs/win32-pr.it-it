---
description: I moduli dei criteri sono programmi che ricevono richieste da Servizi certificati, valutano tali richieste e specificano proprietà facoltative dei certificati compilati per compilare tali richieste.
ms.assetid: 23d920ea-af62-42ce-ad48-c7a03ab55fc9
title: Moduli dei criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11fd84b91b66e811134bb5878bf3a000363aef7bf9321bbff5a23ad3d25158f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978818"
---
# <a name="policy-modules"></a>Moduli dei criteri

I moduli dei criteri sono programmi che ricevono richieste da Servizi certificati, valutano tali richieste e specificano proprietà facoltative dei certificati compilati per compilare tali richieste. Un modulo criteri viene implementato come [*libreria a collegamento dinamico*](../secgloss/d-gly.md) (DLL). Un modulo criteri può usare [l'interfaccia ICertServerPolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) per comunicare con Servizi certificati. Servizi certificati comunica con un modulo criteri tramite chiamate COM dirette o, se il modulo non supporta chiamate COM dirette, tramite Automazione.

Un modulo criteri può visualizzare le proprietà e le estensioni del certificato esistenti e può anche visualizzare gli attributi e le proprietà della richiesta. Inoltre, un modulo criteri può impostare o modificare le estensioni del certificato e le proprietà "NotBefore" e "NotAfter", nonché il nome distinto [*relativo*](../secgloss/r-gly.md) (RDN) di un soggetto del certificato, soggetto a determinate restrizioni. Un modulo criteri infine elava o nega la richiesta [*di certificato*](../secgloss/c-gly.md) o la mantiene in sospeso.

Prima di scrivere un modulo criteri personalizzato, è consigliabile usare uno dei moduli dei criteri predefiniti. Sia l'autorità di [*certificazione*](../secgloss/c-gly.md) (CA) di Servizi certificati che la CA autonoma vengono forniti con un modulo dei criteri predefinito appropriato. I moduli dei criteri predefiniti aziendali e autonomi emettere richieste di certificato (anche se il criterio predefinito autonomo è mantenere il certificato in sospeso fino a quando non viene emesso manualmente da un amministratore). Un'autorità di certificazione aziendale deve usare solo il modulo Criteri aziendali fornito da Microsoft.

La CA globale (enterprise) richiede Active Directory. Altre funzionalità del modulo dei criteri predefinito includono modelli di [*certificato,*](../secgloss/a-gly.md) sicurezza dell'elenco di controllo di accesso (ACL) nei modelli di certificato per garantire che le richieste siano emesse solo alle estensioni autorizzate e predefinite aggiunte al certificato emesso e al supporto per i certificati di accesso al dominio smart card.

Il modulo criteri ca autonomo predefinito non supporta molte delle funzionalità del modulo aziendale predefinito, ma supporta il rilascio di certificati smart card certificati. Per informazioni dettagliate specifiche, nonché le funzionalità più correnti del modulo dei criteri predefinito, vedere la documentazione del prodotto.

Per le installazioni in cui il modulo dei criteri predefinito non è accettabile, Servizi certificati consente moduli di criteri personalizzati. Per altre informazioni, vedere [Scrittura di moduli di criteri personalizzati.](writing-custom-modules.md)

 

 
