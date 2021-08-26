---
description: Il Centro distribuzione chiavi (KDC) viene implementato come servizio di dominio. Usa Active Directory come database degli account e il Catalogo globale per indirizzare le segnalazioni ai KDC in altri domini.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: Centro distribuzione chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eef410ccb9289d30507708dc35000e1c15d5d4c9998b28b33a2e51d1a15b1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013341"
---
# <a name="key-distribution-center"></a>Centro distribuzione chiavi

Il Centro distribuzione chiavi (KDC) viene implementato come servizio di dominio. Usa Active Directory come database degli account e il Catalogo globale per indirizzare le segnalazioni ai KDC in altri domini.

Come in altre implementazioni del protocollo [*Kerberos,*](../secgloss/k-gly.md)il KDC è un singolo processo che fornisce due servizi:

-   Servizio di autenticazione (AS)

    Questo servizio emissione di ticket di concessione ticket (TGT) per la connessione al servizio di concessione ticket nel proprio dominio o in qualsiasi dominio trusted. Prima che un client possa richiedere un ticket a un altro computer, deve richiedere un TGT al servizio di autenticazione nel dominio dell'account del client. Il servizio di autenticazione restituisce un TGT per il servizio di concessione ticket nel dominio del computer di destinazione. Il TGT può essere riutilizzato fino alla scadenza, ma il primo accesso al servizio di concessione ticket di qualsiasi dominio richiede sempre una corsa al servizio di autenticazione nel dominio dell'account del client.

-   Ticket-Granting Service (TGS)

    Questo servizio eta ticket per la connessione ai computer nel proprio dominio. Quando i client vogliono accedere a un computer, contattano il servizio di concessione ticket nel dominio del computer di destinazione, presentano un TGT e chiedono un ticket al computer. Il ticket può essere riutilizzato fino alla scadenza, ma il primo accesso a qualsiasi computer richiede sempre una corsa al servizio di concessione ticket nel dominio dell'account del computer di destinazione.

Il KDC per un dominio si trova in un controller di dominio, così come Active Directory per il dominio. Entrambi i servizi vengono avviati [](../secgloss/l-gly.md) automaticamente dall'autorità di sicurezza locale (LSA) del controller di dominio ed eseguiti come parte del processo di LSA. Nessuno dei due servizi può essere arrestato. Se il KDC non è disponibile per i client di rete, anche Active Directory non è disponibile e il controller di dominio non controlla più il dominio. Il sistema garantisce la disponibilità di questi e di altri servizi di dominio consentendo a ogni dominio di avere diversi controller di dominio, tutti i peer. Qualsiasi controller di dominio può accettare richieste di autenticazione e richieste di concessione di ticket indirizzate al KDC del dominio.

Il [*nome dell'entità*](../secgloss/s-gly.md) di sicurezza usato dal KDC in qualsiasi dominio è "krbtgt", come specificato da [RFC 4120.](https://www.ietf.org/rfc/rfc4120.txt) Un account per questa entità di sicurezza viene creato automaticamente quando viene creato un nuovo dominio. L'account non può essere eliminato né può essere modificato. Un valore casuale della password viene assegnato automaticamente all'account dal sistema durante la creazione del dominio. La password per l'account del KDC viene usata per derivare una chiave crittografica per crittografare e decrittografare i TGT che elava. La password per un account trust di dominio viene usata per derivare una chiave tra aree di autenticazione per crittografare i ticket di riferimento.

Tutte le istanze del KDC all'interno di un dominio usano l'account di dominio per l'entità di sicurezza "krbtgt". I client indirizzano i messaggi al KDC di un dominio includendo sia il nome principale del servizio, "krbtgt" che il nome del dominio. Entrambi gli elementi di informazioni vengono usati anche nei ticket per identificare l'autorità emittente. Per informazioni sui moduli dei nomi e sulle convenzioni di indirizzamento, vedere [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
