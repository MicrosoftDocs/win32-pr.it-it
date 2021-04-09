---
description: Requisiti di persone nelle vicinanze
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: Requisiti di persone nelle vicinanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6afb97800041e0fcd9a10a6d95334b832fb363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881793"
---
# <a name="people-near-me-requirements"></a>Requisiti di persone nelle vicinanze

Per fare in modo che le [persone nelle vicinanze](about-people-near-me.md) forniscano una connettività semplice e una facile collaborazione agli utenti per le applicazioni di rete peer di Windows, è possibile eseguire le operazioni seguenti:

### <a name="people-discovery"></a>Individuazione persone

L'individuazione utenti consente a un utente di individuare e visualizzare il set di peer che si trovano nella subnet locale. Tutti i computer della subnet locale devono annunciare i nomi dei peer connessi. I peer elencati dopo una query di individuazione sono il set di utenti che eseguono Windows Vista configurati per annunciare un nome alternativo ad altri utenti che usano [persone nelle vicinanze](about-people-near-me.md). Questa funzionalità è disabilitata per impostazione predefinita e deve essere abilitata dall'utente che ha eseguito l'accesso.

> [!Note]  
> I peer remoti individuati durante il processo di individuazione "persone nelle vicinanze" non sono necessariamente gli utenti previsti associati ai peer individuati.

 

### <a name="extended-data-discovery"></a>Individuazione dati estesa

L'individuazione dei dati estesi consente la ricerca di utenti con interessi specifici. È anche possibile che gli utenti specifichino che desiderano annunciare dati aggiuntivi su se stessi. Ad esempio, i dati possono delineare specifici interessi professionali in una conferenza di settore, oltre al nome alternativo dell'utente connesso.

### <a name="application-discovery"></a>Individuazione di applicazioni

La natura esatta della collaborazione ad hoc abilitata da persone nelle vicinanze è specifica per le applicazioni. È possibile, ad esempio, che la collaborazione stia chattando o condividendo le foto, richiedendo applicazioni specifiche. Per consentire alle persone nelle vicinanze di abilitare le attività di collaborazione, è necessario pubblicizzare e individuare anche il set di applicazioni disponibili per gli scenari di persone nelle vicinanze.

### <a name="subscription"></a>Subscription

Utilizzando una sottoscrizione, le applicazioni possono sottoscrivere per tenere traccia della presenza, delle applicazioni e delle modifiche agli oggetti di una persona.

### <a name="invitation"></a>Invito

Dopo che gli utenti, gli interessi e le applicazioni sono stati individuati, la collaborazione tra peer, usando un'applicazione di persone nelle vicinanze, può iniziare un scambio di invito e accettazione. Il peer iniziale Invia un messaggio di invito a un altro peer o peer. Gli utenti che ricevono l'invito possono accettare o rifiutare l'invito. Quando l'invito viene accettato, viene avviata l'applicazione peer appropriata per l'attività richiesta.

### <a name="add-as-a-contact"></a>Aggiungi come contatto

Se gli utenti stabiliscono un'attività di collaborazione tramite persone nelle vicinanze e vogliono mantenere il contatto nel tempo, possono aggiungersi come contatto. Una volta eseguita questa operazione, è possibile osservare lo stato di presenza di un utente, ad esempio online, offline o di fuori, e invitarli a un'attività di collaborazione in qualsiasi momento su Internet. Qualsiasi attività che era possibile con la persona che si trovava nelle vicinanze è possibile anche con un contatto tramite Internet.

### <a name="security"></a>Sicurezza

Per proteggere gli utenti e i dati scambiati in un'attività di collaborazione peer, gli utenti hanno il controllo della configurazione sugli elementi che vengono annunciati. Gli utenti devono inoltre accettare un invito prima che possa iniziare la collaborazione tra peer. L'attività di collaborazione viene crittografata con un canale crittografato con Secure Sockets Layer (SSL) (noto anche come Schannel). SSL è un protocollo crittografico per proteggere le comunicazioni basate su TCP. Per ulteriori informazioni, vedere [Schannel](windows-vista-components-for-people-near-me.md). Questi requisiti sono supportati da un nuovo set di componenti nell'architettura di [rete peer di Windows](what-is-peer-networking-.md)in Windows Vista.

 

 



