---
title: Informazioni sull'implementazione di Microsoft WinSNMP
description: L'implementazione di Microsoft WinSNMP è conforme a WinSNMP versione 2.0.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693a2fd5c6aa21d684d485f75b04160e72bfe1455c13ef8c320c863b61ab696b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009869"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a>Informazioni sull'implementazione di Microsoft WinSNMP

L'implementazione di Microsoft WinSNMP è conforme a WinSNMP versione 2.0. Supporta tutte le funzioni e le operazioni definite sia nella specifica WinSNMP versione 1.1a che in WinSNMP versione 2.0 Addendum. L'implementazione fornisce i servizi seguenti per le applicazioni WinSNMP:

-   Gestisce le comunicazioni da e verso le entità di gestione. L'entità può risiedere nel computer locale o essere connessa tramite una rete locale o wide area o Internet. Per altre informazioni, vedere [Livelli di supporto SNMP.](levels-of-snmp-support.md)
-   Nasconde i dettagli del protocollo SNMP, della notazione della sintassi astratta (ASN.1) e delle regole di codifica di base (BER) per descrivere la sintassi di trasferimento.
-   Verifica la correttezza delle PDU e rifiuta le PDU non valide. Per altre informazioni, vedere [Uso delle unità dati del protocollo](working-with-protocol-data-units.md).
-   Trasforma i tipi di PDU SNMPv2C quando necessario in base alle RFC pertinenti.
-   Converte trap SNMPv1 da un agente SNMPv1 a trap SNMPv2C in base a RFC 1908, "Coesistenza tra la versione 1 e la versione 2 di Internet-standard Network Management Framework". Per altre informazioni, vedere [Traduzione di trap da SNMPv1 a SNMPv2C.](translating-traps-from-snmpv1-to-snmpv2c.md)
-   Supporta i criteri di ritrasmissione dell'applicazione e fornisce il supporto per l'esecuzione della ritrasmissione. Per altre informazioni, vedere [Database WinSNMP](the-winsnmp-database.md) e [Informazioni sulla ritrasmissione.](about-retransmission.md)
-   Fornisce il supporto per la conversione di entità e contesto per l'applicazione. Per altre informazioni, vedere [Database WinSNMP](the-winsnmp-database.md) e [Impostazione della modalità di conversione](setting-the-entity-and-context-translation-mode.md)di entità e contesto.

Per altre informazioni sulla relazione tra un'applicazione WinSNMP e l'implementazione, vedere Concetti di Gestione dati [WinSNMP](winsnmp-data-management-concepts.md) e [Sessioni WinSNMP](winsnmp-sessions.md).

 

 




