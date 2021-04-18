---
description: "L'API di raggruppamento usa le funzioni seguenti:"
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Raggruppamento di funzioni API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312273"
---
# <a name="grouping-api-functions"></a>Raggruppamento di funzioni API

L'API di raggruppamento usa le funzioni seguenti:

## <a name="group-initialization-and-cleanup-functions"></a>Funzioni di inizializzazione e pulizia del gruppo



| Funzione                                       | Descrizione                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | Chiude un gruppo peer creato con [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) ed Elimina tutte le risorse allocate. |
| [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | Avvia un gruppo peer utilizzando una versione richiesta dell'infrastruttura peer.                                        |



 

## <a name="group-creation-and-access-functions"></a>Funzioni di creazione e accesso del gruppo



| Funzione                                                                       | Descrizione                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | Invalida l'handle del gruppo peer ottenuto da una chiamata precedente alla funzione [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) . |
| [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | Avvia una ricerca PNRP per un gruppo peer e tenta di connettersi a tale gruppo. Quando questa funzione viene chiamata correttamente, un peer può comunicare con altri membri del gruppo peer.                             |
| [**PeerGroupConnectByAddress**](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | Tenta di connettersi al gruppo peer a cui partecipano altri peer con indirizzi IPv6 noti.                                                                                                       |
| [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | Consente di creare un nuovo gruppo peer.                                                                                                                                                                                    |
| [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | Restituisce una stringa XML che può essere utilizzata dal peer specificato per partecipare a un gruppo.                                                                                                                                |
| [**PeerGroupCreatePasswordInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | Restituisce una stringa XML che può essere utilizzata dal peer specificato per unire in join un gruppo con una password corrispondente.                                                                                                       |
| [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | Elimina i dati locali e il certificato associato a un gruppo peer.                                                                                                                                         |
| [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | Recupera lo stato corrente di un gruppo.                                                                                                                                                                     |
| [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | Rilascia le credenziali, incluso un GMC, a un'identità specifica e, facoltativamente, restituisce una stringa XML di invito che il peer invitato può utilizzare per aggiungere un gruppo peer.                                                  |
| [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | Consente a un peer con invito a partecipare a un gruppo peer esistente.                                                                                                                                             |
| [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | Apre un gruppo peer creato o aggiunto da un peer.                                                                                                                                                        |
| [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | Restituisce una struttura di [**\_ \_ informazioni di invito peer**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) con i dettagli di un invito specifico.                                                                                        |
| [**PeerGroupPasswordJoin**](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | Consente a un peer con un invito e la password corretta di partecipare a un gruppo peer protetto da password.                                                                                                           |



 

## <a name="group-and-member-information-functions"></a>Funzioni di informazioni sui membri e sui gruppi



| Funzione                                                 | Descrizione                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | Crea un'enumerazione dei membri del gruppo peer disponibili e le informazioni di appartenenza associate.                                  |
| [**PeerGroupGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | Recupera le informazioni sulle proprietà di un gruppo specificato.                                                                      |
| [**PeerGroupSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | Imposta le proprietà del gruppo peer corrente. Nella versione 1,0 di questa API, solo l'autore del gruppo peer può eseguire questa operazione. |



 

## <a name="records-and-record-management-functions"></a>Record e funzioni di gestione dei record



| Funzione                                                 | Descrizione                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | Aggiunge un nuovo record al gruppo peer, che viene propagato a tutti i peer partecipanti. |
| [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | Elimina un record da un gruppo peer. Solo l'autore di un record può eliminarlo.      |
| [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | Crea un'enumerazione di record di gruppi di peer.                                        |
| [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | Recupera un record di gruppo specifico.                                                   |
| [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | Esegue una ricerca nel database del gruppo peer locale per i record che corrispondono ai criteri specificati. |
| [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | Aggiorna un record in un gruppo peer specifico.                                       |



 

## <a name="group-database-importexport-functions"></a>Funzioni di importazione/esportazione di database di gruppo



| Funzione                                                   | Descrizione                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | Esporta un database del gruppo peer in un file specifico, che può essere trasportato in un altro computer e importato con la funzione [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) . |
| [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | Importa un database del gruppo peer da un file locale.                                                                                                                                          |



 

## <a name="direct-connection-functions"></a>Funzioni di connessione diretta



| Funzione                                                                 | Descrizione                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | Chiude una connessione diretta specifica tra due peer.              |
| [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | Crea un'enumerazione delle connessioni attualmente attive nel peer. |
| [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | Stabilisce una connessione diretta con un altro peer in un gruppo peer.  |
| [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | Invia dati a un membro tramite una connessione diretta o adiacente.        |



 

## <a name="group-events-infrastructure"></a>Infrastruttura degli eventi di gruppo



| Funzione                                                     | Descrizione                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | Consente a un'applicazione di recuperare i dati restituiti da un evento di raggruppamento.                       |
| [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | Registra un peer per eventi specifici del gruppo peer.                                               |
| [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | Annulla la registrazione di un peer dalla notifica degli eventi peer associati all'handle di evento fornito. |



 

## <a name="group-time-conversion-functions"></a>Funzioni di conversione dell'ora del gruppo



| Funzione                                                                     | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | Converte il valore dell'ora di riferimento gestito dal gruppo peer in un valore di ora localizzato appropriato per la visualizzazione in un computer peer. |
| [**PeerGroupUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | Converte un valore dell'ora locale dal computer di un peer a un valore di ora del gruppo peer comune.                                         |



 

## <a name="group-configuration-functions"></a>Funzioni di configurazione del gruppo



| Funzione                                               | Descrizione                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | Esporta la configurazione di gruppo per un peer come stringa XML che contiene l'identità, il nome del gruppo e il GMC per l'identità. |
| [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | Importa una configurazione del gruppo peer per un'identità in base alle impostazioni specifiche in una stringa di configurazione XML specificata.         |



 

 

 



