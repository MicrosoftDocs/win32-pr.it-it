---
description: 'Modello concettuale: requisiti delle applicazioni'
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: 'Modello concettuale: requisiti delle applicazioni'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a287ff940f154bf104bbb50f6362bf573d9223
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127135"
---
# <a name="the-conceptual-model-application-requirements"></a>Modello concettuale: requisiti delle applicazioni

Quando si progetta il modello concettuale, è necessario definire i problemi aziendali e le funzioni necessarie per risolvere tali problemi. Un approccio basato su procedure consigliate consiste nel comunicare con persone che utilizzeranno effettivamente l'applicazione, con una vasta gamma di utenti e con il maggior numero possibile di scenari aziendali o utente. Determinare le identità e il numero dei potenziali utenti del sistema, nonché le dimensioni e l'ambito dei dati necessari. Sebbene la raccolta di queste informazioni possa essere l'aspetto meno tecnico del processo di progettazione, è uno dei più importanti. Per sviluppare un'applicazione corretta, è necessario conoscere chiaramente i problemi e i processi aziendali che devono essere risolti.

Quando si determinano i requisiti dell'applicazione, tenere presenti le considerazioni seguenti:

-   Requisiti di prestazioni. Qual è il tempo di risposta previsto per le attività dell'applicazione? Quale supporto del failover per i server inattivi è necessario? Quali sono le ore di disponibilità?
-   Ambiente. Quali server sono disponibili? Server aggiuntivi pianificati per gestire i requisiti di scalabilità?
-   Distribuzione. In che modo l'applicazione si integrerà con un sistema corrente? Quali altri sistemi interagiranno con l'applicazione? Quali sistemi operativi usano gli altri sistemi? Quali protocolli di comunicazione devono essere supportati? Quale API è possibile usare per interagire con gli altri sistemi? Dove si trovano gli altri sistemi in rete? Quali sono le restrizioni sull'uso del computer? Quali account utente sono autorizzati ad accedere?
-   Posizione. Dove si trovano i dati in relazione al client? I dati sono accessibili in remoto o sono locali?
-   Sicurezza. Sono previsti requisiti di crittografia o verifica dell'integrità? Sono previsti requisiti per l'autenticazione o la protezione dei dati?
-   Diritti di accesso. Esistono vincoli su chi è autorizzato a eseguire determinate operazioni? In tal caso, è necessario innanzitutto documentare le operazioni che richiedono l'autorizzazione e quindi documentare i tipi di utenti che possono avere l'autorizzazione. Questi requisiti possono avere un notevole effetto sul modo in cui vengono implementate le parti dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello logico: definizione dell'applicazione e pianificazione](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[Modello fisico: architettura dell'applicazione](the-physical-model--application-architecture.md)
</dt> </dl>

 

 



