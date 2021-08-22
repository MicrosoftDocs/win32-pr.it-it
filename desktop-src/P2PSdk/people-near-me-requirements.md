---
description: Persone nelle vicinanze requisiti
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: Persone nelle vicinanze requisiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebbb904175184b6e9d06c807aa4b4ed645c93633114d6b9b64085e34dfa3683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518351"
---
# <a name="people-near-me-requirements"></a>Persone nelle vicinanze requisiti

Per consentire [Persone nelle vicinanze](about-people-near-me.md) connettività senza problemi e una facile collaborazione agli utenti per le applicazioni di rete Windows peer, si ottiene quanto segue:

### <a name="people-discovery"></a>Individuazione persone

People Discovery consente a un utente di individuare e visualizzare il set di peer che si trovano nella subnet locale. Tutti i computer nella subnet locale devono annunciare i nomi dei peer connessi. I peer elencati dopo una query di individuazione sono il set di utenti che eseguono Windows Vista configurati per annunciare un nome alternativo ad altri utenti [usando Persone nelle vicinanze](about-people-near-me.md). Questa funzionalità è disabilitata per impostazione predefinita e deve essere abilitata dall'utente connesso.

> [!Note]  
> I peer remoti individuati durante il processo di individuazione Persone nelle vicinanze non sono necessariamente gli utenti previsti associati ai peer individuati.

 

### <a name="extended-data-discovery"></a>Individuazione dati estesa

L'individuazione dati estesa consente la ricerca di utenti con interessi specifici. È anche possibile che gli utenti specificano di voler annunciare dati aggiuntivi su se stessi. Ad esempio, i dati potrebbero delineare interessi professionali specifici in una conferenza di settore, oltre al nome alternativo dell'utente connesso.

### <a name="application-discovery"></a>Individuazione applicazioni

La natura esatta della collaborazione ad hoc abilitata Persone nelle vicinanze è specifica delle applicazioni. Ad esempio, la collaborazione potrebbe essere la chat o la condivisione di foto, entrambe che richiedono applicazioni specifiche. Per consentire Persone nelle vicinanze le attività di collaborazione, anche il set di applicazioni disponibili per gli scenari Persone nelle vicinanze deve essere annunciato e individuabile.

### <a name="subscription"></a>Subscription

Usando una sottoscrizione, le applicazioni possono sottoscrivere per tenere traccia della presenza, delle applicazioni e delle modifiche agli oggetti di una persona.

### <a name="invitation"></a>Invito

Dopo aver individuato le persone, gli interessi e le applicazioni, la collaborazione tra peer, tramite un'applicazione Persone nelle vicinanze, può iniziare uno scambio di invito e accettazione. Il peer di avvio invia un messaggio di invito a un altro peer o peer. Gli utenti che ricevono l'invito possono accettare o rifiutare l'invito. Quando l'invito viene accettato, viene avviata l'applicazione peer appropriata per l'attività richiesta.

### <a name="add-as-a-contact"></a>Aggiungi come contatto

Se gli utenti stabiliscono un'attività di collaborazione tramite Persone nelle vicinanze e vogliono mantenere il contatto nel tempo, possono aggiungersi reciprocmente come contatto. Una volta eseguita questa operazione, può osservare lo stato di presenza di un utente (ad esempio online, offline o non disponibile) e invitarlo a un'attività di collaborazione in qualsiasi momento su Internet. Qualsiasi attività che era possibile eseguire con la persona che si trovava nelle vicinanze è possibile anche con un contatto tramite Internet.

### <a name="security"></a>Sicurezza

Per proteggere gli utenti e i dati s scambiati in un'attività di collaborazione tra peer, gli utenti hanno il controllo della configurazione su ciò che viene annunciato. Gli utenti devono anche accettare un invito prima di poter iniziare la collaborazione tra peer. L'attività di collaborazione viene crittografata con un canale Secure Sockets Layer (SSL) crittografato (noto anche come Schannel). SSL è un protocollo di crittografia per proteggere le comunicazioni basate su TCP. Per altre informazioni, vedere [SChannel.](windows-vista-components-for-people-near-me.md) Questi requisiti sono supportati da un nuovo set di componenti [nell'architettura Windows peer in](what-is-peer-networking-.md)Windows Vista.

 

 



