---
description: Quando un pacchetto di sicurezza SSP/AP funziona come pacchetto di autenticazione, viene caricato nello spazio di processo dell'autorità di protezione locale (LSA) e viene definito in modalità LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Modalità LSA rispetto alla modalità utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058036"
---
# <a name="lsa-mode-vs-user-mode"></a>Modalità LSA rispetto alla modalità utente

Quando un pacchetto di [*sicurezza*](../secgloss/s-gly.md) SSP/AP funziona come [*pacchetto di autenticazione*](../secgloss/a-gly.md), viene caricato nello spazio di processo dell'autorità di [*protezione locale*](../secgloss/l-gly.md) (LSA) e viene definito in modalità LSA. Le applicazioni di accesso accedono alla funzionalità del pacchetto di autenticazione tramite le [funzioni di accesso LSA](authentication-functions.md). Gli sviluppatori possono utilizzare le funzioni di supporto LSA disponibili solo per i pacchetti di sicurezza in modalità LSA per implementare pacchetti di autenticazione più sofisticati rispetto a quelli precedentemente supportati.

Quando un [*pacchetto di sicurezza*](../secgloss/s-gly.md) fornisce servizi di sicurezza a un'applicazione client/server, viene caricato nei processi client e server e viene definito in modalità utente. Le applicazioni client/server accedono ai servizi di supporto per la sicurezza del pacchetto di sicurezza tramite Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI).

Il supporto LSA per SSP/APs include funzioni che possono essere utilizzate dalle istanze in modalità LSA e in modalità utente di un pacchetto di sicurezza per la comunicazione. Inoltre, l'istanza in modalità utente di un pacchetto di sicurezza può delegare le richieste selezionate per le informazioni all'istanza in modalità LSA del pacchetto.

Per informazioni dettagliate sull'inizializzazione dei pacchetti di sicurezza per ogni modalità, vedere [inizializzazione in modalità LSA](lsa-mode-initialization.md) e [inizializzazione in modalità utente](user-mode-initialization.md).

 

 
