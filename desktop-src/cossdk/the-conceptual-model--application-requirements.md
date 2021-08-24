---
description: "Modello concettuale: requisiti dell'applicazione"
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: "Modello concettuale: requisiti dell'applicazione"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19c69f8da7179765242815c4d01760c36b94e95714188f7db772600826d0416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853921"
---
# <a name="the-conceptual-model-application-requirements"></a>Modello concettuale: requisiti dell'applicazione

Quando si progetta il modello concettuale, è necessario definire i problemi aziendali e le funzioni necessarie per risolverli. Un approccio basato sulle procedure consigliate consiste nel parlare con persone che useranno effettivamente l'applicazione, incontrare un'ampia gamma di utenti e includere il maggior numero possibile di scenari aziendali o utente. Determinare le identità e il numero dei potenziali utenti del sistema, nonché le dimensioni e l'ambito dei dati coinvolti. Sebbene la raccolta di queste informazioni possa essere l'aspetto meno tecnico del processo di progettazione, è uno dei più importanti. Per sviluppare correttamente un'applicazione, è necessaria una conoscenza chiara dei problemi aziendali e dei processi che devono essere affrontati.

Quando si determinano i requisiti dell'applicazione, tenere presenti le considerazioni seguenti:

-   Requisiti di prestazioni. Qual è il tempo di risposta previsto per le attività dell'applicazione? Quale supporto di failover per i server in servizio è necessario? Quali sono le ore di disponibilità?
-   Ambiente. Quali server sono disponibili? Sono pianificati server aggiuntivi per gestire eventuali requisiti di scalabilità?
-   Distribuzione. In che modo l'applicazione si integrerà con un sistema corrente? Con quali altri sistemi interagirà l'applicazione? Quali sistemi operativi usano gli altri sistemi? Quali protocolli di comunicazione devono essere supportati? Quale API è possibile usare per interagire con gli altri sistemi? Dove si trovano gli altri sistemi nella rete? Quali restrizioni sull'uso del computer sono applicate? A quali account utente è consentito l'accesso?
-   Posizione. Dove si trovano i dati in relazione al client? I dati sono accessibili in remoto o sono locali?
-   Sicurezza. Sono presenti requisiti di crittografia o controllo dell'integrità? Esistono requisiti di autenticazione o protezione dei dati?
-   Diritti di accesso. Esistono vincoli su chi è autorizzato a eseguire determinate operazioni? In tal caso, è necessario prima documentare le operazioni che richiedono l'autorizzazione e quindi documentare i tipi di utenti che possono avere l'autorizzazione. Questi requisiti possono avere un notevole impatto sulla modalità di implementazione delle parti dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello logico: definizione e pianificazione dell'applicazione](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[Modello fisico: Architettura dell'applicazione](the-physical-model--application-architecture.md)
</dt> </dl>

 

 



