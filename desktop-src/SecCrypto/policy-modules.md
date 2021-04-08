---
description: I moduli criteri sono programmi che ricevono richieste dai servizi certificati, valutano tali richieste e specificano le proprietà facoltative dei certificati compilati per colmare tali richieste.
ms.assetid: 23d920ea-af62-42ce-ad48-c7a03ab55fc9
title: Moduli criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781a88ab714c402ea1670ac8c18ae4d80eb776e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968387"
---
# <a name="policy-modules"></a>Moduli criteri

I moduli criteri sono programmi che ricevono richieste dai servizi certificati, valutano tali richieste e specificano le proprietà facoltative dei certificati compilati per colmare tali richieste. Un modulo criteri viene implementato come [*libreria a collegamento dinamico*](../secgloss/d-gly.md) (dll). Un modulo criteri può usare l'interfaccia [ICertServerPolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) per comunicare con i servizi certificati. Servizi certificati comunica con un modulo criteri per mezzo di chiamate COM dirette o, se il modulo non supporta le chiamate COM dirette, per mezzo dell'automazione.

Un modulo criteri può visualizzare le estensioni e le proprietà dei certificati esistenti e può anche visualizzare gli attributi e le proprietà della richiesta. Inoltre, un modulo criteri può impostare o modificare le estensioni dei certificati e le proprietà "NotBefore" e "NotAfter", nonché il [*nome distinto relativo*](../secgloss/r-gly.md) (RDN) di un soggetto del certificato, soggetto a determinate restrizioni. Un modulo criteri in definitiva rilascia o nega la [*richiesta di certificato*](../secgloss/c-gly.md) o la mantenga in sospeso.

Prima di scrivere un modulo criteri personalizzato, provare a usare uno dei moduli criteri predefiniti. Sia l' [*autorità di certificazione*](../secgloss/c-gly.md) dell'organizzazione (CA) che la CA autonoma vengono fornite con un modulo criteri predefinito appropriato. I moduli criteri predefiniti Enterprise e autonomo emettono richieste di certificato (sebbene i criteri predefiniti autonomi contengano il certificato in sospeso fino a quando non viene emesso manualmente da un amministratore). Un'autorità di certificazione dell'organizzazione deve usare solo il modulo criteri di organizzazione fornito da Microsoft.

La CA globale (Enterprise) richiede Active Directory. Le funzionalità aggiuntive del modulo criteri predefinito includono i modelli di certificato, la sicurezza dell' [*elenco di controllo di accesso*](../secgloss/a-gly.md) (ACL) sui modelli di certificato per garantire che le richieste vengano rilasciate solo alle estensioni autorizzate e predefinite aggiunte al certificato emesso e al supporto per i certificati di accesso al dominio delle smart card.

Il modulo criteri CA autonomo predefinito non supporta molte delle funzionalità del modulo Enterprise predefinito, ma supporta l'emissione di certificati per smart card. Per dettagli specifici e per le funzionalità più recenti del modulo criteri predefinito, vedere la documentazione del prodotto.

Per le installazioni in cui il modulo criteri predefinito non è accettabile, Servizi certificati consente i moduli criteri personalizzati. Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di moduli criteri personalizzati](writing-custom-modules.md).

 

 
