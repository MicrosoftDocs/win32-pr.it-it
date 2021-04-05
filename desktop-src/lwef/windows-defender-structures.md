---
title: Strutture di Windows Defender
description: Strutture usate dalle app quando si chiama per richiedere analisi, aggiornamenti delle firme o informazioni da Windows Defender.
ms.assetid: EF4116D3-DA50-4078-A024-2D624945D8C1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d690de552137ce267b9d1d7a9cec711b161528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708956"
---
# <a name="windows-defender-structures"></a>Strutture di Windows Defender

Strutture usate dalle app quando si chiama per richiedere analisi, aggiornamenti delle firme o informazioni da Windows Defender.



| Struttura                                                      | Descrizione                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**\_dati MPCALLBACK**](mpcallback-data.md)                    | Dati passati alla funzione di callback.<br/>                                        |
| [**\_dati MPCLEAN**](mpclean-data.md)                          | Dati di notifica passati alla funzione di callback pulita.<br/>                         |
| [**MPCLEAN \_ i dati di PREverifica \_**](mpclean-precheck-data.md)       | Dati di notifica passati per pulire la funzione di callback di verifica.<br/>                |
| [**\_stato MPCOMPONENT**](mpcomponent-status.md)              | Informazioni sullo stato del componente.<br/>                                                |
| [**versione di MPCOMPONENT \_**](mpcomponent-version.md)            | Tempo di aggiornamento e versione per un singolo componente.<br/>                         |
| [**\_dati MPCONFIGURATION**](mpconfiguration-data.md)          | Contiene i dati sulle modifiche di configurazione, inclusi i vecchi e i nuovi valori.<br/> |
| [**\_dati MPENDOFLIFE**](mpendoflife-data.md)                  | Dati di notifica di "fine vita".<br/>                                             |
| [**\_dati MPEXPIRATION**](mpexpiration-data.md)                | Notifica sullo stato di scadenza del prodotto.<br/>                                      |
| [**\_dati MPFASTPATH**](mpfastpath-data.md)                    | Notifica di aggiornamento FastPath.<br/>                                                |
| [**\_dati MPHEALTH**](mphealth-data.md)                        | Dati di notifica dell'integrità.<br/>                                                    |
| [**\_dati MPMALWARETOAST**](mpmalwaretoast-data.md)            | Dati di notifica di tipo avviso popup malware.<br/>                                             |
| [**MPNIS \_ \_ dati privati**](mpnis-private-data.md)             | Notifiche NIS private.<br/>                                                   |
| [**\_dati MPRESERVED**](mpreserved-data.md)                    | Dati di notifica riservati.<br/>                                                  |
| [**\_informazioni MPRESOURCE**](mpresource-info.md)                    | Struttura delle informazioni sulle risorse.<br/>                                              |
| [**\_statistiche MPRESOURCE**](mpresource-stats.md)                  | Statistiche correlate alle risorse.<br/>                                                 |
| [**\_dati MPSAMPLE**](mpsample-data.md)                        | Dati di notifica passati alla funzione di callback di invio dell'esempio.<br/>         |
| [**\_dati MPSCAN**](mpscan-data.md)                            | Analizza i dati passati al callback.<br/>                                            |
| [**risorse di MPSCAN \_**](mpscan-resources.md)                  | Informazioni sulle risorse passate durante un'operazione di analisi.<br/>                         |
| [**risultato di MPSCAN \_**](mpscan-result.md)                        | Risultati di un'analisi.<br/>                                                       |
| [**\_dati MPSIGUPDATE**](mpsigupdate-data.md)                  | Dati di notifica passati alla funzione di callback dell'aggiornamento della firma.<br/>          |
| [**\_dati MPSTATUS**](mpstatus-data.md)                        | Contiene dati sullo stato corrente di un componente del prodotto.<br/>        |
| [**MPSTATUS \_ DATAEX non \_ usato**](mpstatus-dataex-unused.md)     | Struttura fittizia per non-SRP.<br/>                                                 |
| [**\_informazioni MPSTATUS**](mpstatus-info.md)                        | Informazioni sullo stato di malware Protection Manager.<br/>                       |
| [**\_dati MPTHREAT**](mpthreat-data.md)                        | Dati di notifica passati a causa di rilevamento o modifica delle minacce.<br/>            |
| [**\_informazioni MPTHREAT**](mpthreat-info.md)                        | Contiene informazioni su una minaccia.<br/>                                         |
| [**\_comportamento INFOEX \_ MPTHREAT**](mpthreat-infoex-behavior.md) | Contiene informazioni specifiche relative alla modifica del comportamento.<br/>                         |
| [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)           | Contiene informazioni specifiche di NIS.<br/>                                           |
| [**MPTHREAT \_ INFOEX non \_ usato**](mpthreat-infoex-unused.md)     | Struttura fittizia per le minacce del tipo di modifica non del comportamento.<br/>                  |
| [**\_informazioni localizzate MPTHREAT \_**](mpthreat-localized-info.md)   | Informazioni localizzate per una minaccia.<br/>                                          |
| [**\_statistiche MPTHREAT**](mpthreat-stats.md)                      | Statistiche correlate alle minacce.<br/>                                                   |
| [**\_dati statistiche \_ MPTHREAT**](mpthreat-stats-data.md)           | Dati aggiuntivi sulle statistiche sulle minacce.<br/>                                           |
| [**\_informazioni MPVERSION**](mpversion-info.md)                      | Informazioni sulla versione per i componenti di malware Protection Manager.<br/>         |



 

 

 





