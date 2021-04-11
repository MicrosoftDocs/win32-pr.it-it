---
description: Windows Sockets 2 offre un set di operazioni espanse che possono essere eseguite in modo coincidente con la creazione di una connessione socket. I requisiti del provider di servizi per l'implementazione di queste funzionalità sono descritti di seguito.
ms.assetid: fbc7055e-ea25-4d17-8039-f0fef300353c
title: Funzionalità avanzate al momento della connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33c6d7ee928fe7e97f535363e9e842285eef7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129199"
---
# <a name="enhanced-functionality-at-connect-time"></a>Funzionalità avanzate al momento della connessione

Windows Sockets 2 offre un set di operazioni espanse che possono essere eseguite in modo coincidente con la creazione di una connessione socket. I requisiti del provider di servizi per l'implementazione di queste funzionalità sono descritti di seguito.

## <a name="conditional-acceptance"></a>Accettazione condizionale

Come descritto in precedenza, [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) richiama una funzione di condizione fornita dal client che usa parametri di input per fornire informazioni sulla richiesta di connessione in sospeso. Queste informazioni possono essere usate dal client per accettare o rifiutare una richiesta di connessione in base a informazioni sul chiamante, ad esempio identificatore del chiamante, QoS e così via. Se la funzione Condition restituisce CF \_ Accept, viene creato un nuovo socket con le stesse proprietà del socket in ascolto e viene restituito un handle per il nuovo socket. Se la funzione Condition restituisce il \_ rifiuto CF, la richiesta di connessione deve essere rifiutata. Se la funzione Condition restituisce CF \_ rinvia, la decisione Accept/Reject non può essere eseguita immediatamente e il provider di servizi deve lasciare la richiesta di connessione nella coda di backlog. Il client deve chiamare di nuovo **WSPAccept** , quando è pronto per prendere una decisione e disporre che la funzione Condition restituisca il valore CF \_ Accept o CF \_ Reject. Mentre una richiesta di connessione posticipata si trova nella parte superiore della coda di backlog, il provider di servizi non rilascia altre indicazioni per le richieste di connessione in sospeso.

## <a name="exchanging-user-data-at-connect-time"></a>Scambio di dati utente al momento della connessione

Alcuni protocolli consentono lo scambio di una piccola quantità di dati utente al momento della connessione. Se tali dati sono stati ricevuti dall'host che esegue la connessione, vengono inseriti in un buffer del provider di servizi e un puntatore a questo buffer insieme a un valore length viene fornito al client Winsock SPI attraverso parametri di input per la funzione di condizione [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) . Se il client Winsock SPI dispone di dati di risposta da restituire all'host che esegue la connessione, può copiarlo in un buffer fornito dal provider di servizi. Un puntatore a questo buffer e un intero che indica le dimensioni del buffer vengono forniti anche come parametri di input della funzione della condizione (se supportati dal protocollo).

## <a name="establishing-socket-groups"></a>Creazione di gruppi di socket

Tutti gli utilizzi dei gruppi di socket sono riservati.

 

 



