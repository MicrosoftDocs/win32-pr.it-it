---
description: Il Centro distribuzione chiavi (KDC) viene implementato come un servizio del dominio. Usa la Active Directory come database di account e il catalogo globale per indirizzare i riferimenti a KDC in altri domini.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: Centro distribuzione chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f473fc3b84fed05e157fa700e7549f025979a90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050138"
---
# <a name="key-distribution-center"></a>Centro distribuzione chiavi

Il Centro distribuzione chiavi (KDC) viene implementato come un servizio del dominio. Usa la Active Directory come database di account e il catalogo globale per indirizzare i riferimenti a KDC in altri domini.

Come in altre implementazioni del [*protocollo Kerberos*](../secgloss/k-gly.md), il KDC è un singolo processo che fornisce due servizi:

-   Servizio di autenticazione (AS)

    Questo servizio emette ticket di concessione ticket (TGT) per la connessione al servizio di concessione ticket in un dominio o in un dominio trusted. Prima che un client possa richiedere un ticket a un altro computer, deve richiedere un TGT dal servizio di autenticazione nel dominio dell'account del client. Il servizio di autenticazione restituisce un TGT per il servizio di concessione ticket nel dominio del computer di destinazione. Il TGT può essere riutilizzato fino alla scadenza, ma il primo accesso al servizio di concessione ticket del dominio richiede sempre un viaggio al servizio di autenticazione nel dominio dell'account del client.

-   Servizio Ticket-Granting (TGS)

    Questo servizio rilascia ticket per la connessione ai computer nel proprio dominio. Quando i client desiderano accedere a un computer, contattano il servizio di concessione ticket nel dominio del computer di destinazione, presentano un TGT e richiedono un ticket al computer. È possibile riutilizzare il ticket fino alla scadenza, ma il primo accesso a qualsiasi computer richiede sempre un viaggio al servizio di concessione ticket nel dominio dell'account del computer di destinazione.

Il KDC per un dominio si trova in un controller di dominio, così come il Active Directory per il dominio. Entrambi i servizi vengono avviati automaticamente dall'autorità di [*protezione locale*](../secgloss/l-gly.md) (LSA) del controller di dominio ed eseguiti come parte del processo di LSA. Nessun servizio può essere arrestato. Se il KDC non è disponibile per i client di rete, anche il Active Directory non è disponibile e il controller di dominio non controlla più il dominio. Il sistema garantisce la disponibilità di questi e altri servizi di dominio consentendo a ogni dominio di avere più controller di dominio, tutti peer. Qualsiasi controller di dominio può accettare richieste di autenticazione e richieste di concessione ticket inviate al KDC del dominio.

Il nome dell' [*entità di sicurezza*](../secgloss/s-gly.md) usato dal KDC in qualsiasi dominio è "krbtgt", come specificato da [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt). Un account per questa entità di sicurezza viene creato automaticamente quando viene creato un nuovo dominio. Non è possibile eliminare l'account né modificare il nome. Un valore di password casuale viene assegnato automaticamente all'account dal sistema durante la creazione del dominio. La password per l'account del KDC viene usata per derivare una chiave crittografica per la crittografia e la decrittografia del TGT che rilascia. La password di un account di trust di dominio viene utilizzata per derivare una chiave tra aree di autenticazione per crittografare i ticket di riferimento.

Tutte le istanze del KDC all'interno di un dominio utilizzano l'account di dominio per l'entità di sicurezza "krbtgt". I client indirizzano i messaggi al KDC di un dominio includendo sia il nome principale del servizio, "krbtgt", sia il nome del dominio. Entrambi gli elementi di informazioni vengono usati anche nei ticket per identificare l'autorità emittente. Per informazioni sui moduli nome e le convenzioni di indirizzamento, vedere [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
