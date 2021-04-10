---
title: Informazioni sull'implementazione di Microsoft WinSNMP
description: L'implementazione di Microsoft WinSNMP è conforme alla versione 2,0 di WinSNMP.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955063"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a>Informazioni sull'implementazione di Microsoft WinSNMP

L'implementazione di Microsoft WinSNMP è conforme alla versione 2,0 di WinSNMP. Supporta tutte le funzioni e le operazioni definite in WinSNMP versione 1.1 a specifica e WinSNMP versione 2,0 addendum. L'implementazione fornisce i servizi seguenti per le applicazioni WinSNMP:

-   Gestisce le comunicazioni da e verso le entità di gestione. L'entità può risiedere nel computer locale o essere connessa tramite una rete locale o wide-area o Internet. Per ulteriori informazioni, vedere [livelli di supporto SNMP](levels-of-snmp-support.md).
-   Nasconde i dettagli del protocollo SNMP, Abstract Syntax Notation One (ASN. 1) e le regole di codifica di base (BER) per la descrizione della sintassi di trasferimento.
-   Verifica la correttezza di PDU e rifiuta PDU non validi. Per altre informazioni, vedere [Working with Protocol Data Units](working-with-protocol-data-units.md).
-   Trasforma i tipi SNMPv2C PDU quando necessario in conformità con le RFC pertinenti.
-   Converte SNMPv1 TRAP da un agente SNMPv1 a trap SNMPv2C in conformità con RFC 1908, "coesistenza tra la versione 1 e la versione 2 del Framework di gestione della rete Internet standard". Per ulteriori informazioni, vedere la pagina relativa [alla conversione di trap da SNMPv1 a SNMPv2c](translating-traps-from-snmpv1-to-snmpv2c.md).
-   Supporta i criteri di ritrasmissione dell'applicazione e fornisce il supporto per l'esecuzione di ritrasmissione. Per ulteriori informazioni, vedere [il database WinSNMP](the-winsnmp-database.md) e [informazioni sulla ritrasmissione](about-retransmission.md).
-   Fornisce supporto per l'entità e la conversione del contesto per l'applicazione. Per ulteriori informazioni, vedere [il database WinSNMP](the-winsnmp-database.md) e [impostazione della modalità di conversione dell'entità e del contesto](setting-the-entity-and-context-translation-mode.md).

Per ulteriori informazioni sulla relazione tra un'applicazione WinSNMP e l'implementazione di, vedere [WinSNMP gestione dati Concepts](winsnmp-data-management-concepts.md) e [WinSNMP Sessions](winsnmp-sessions.md).

 

 




