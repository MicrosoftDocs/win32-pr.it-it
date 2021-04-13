---
description: Descrive il processo di un'operazione di I/O di rete in Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Descrizione di un'operazione di I/O di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345801"
---
# <a name="description-of-a-network-io-operation"></a>Descrizione di un'operazione di I/O di rete

Nella figura seguente viene illustrato il processo di un'operazione di I/O di rete in Windows.

![operazione di i/o di rete in Windows](images/fig4.png)

Quando un'applicazione chiama una funzione di I/O di file per accedere a un file in un computer remoto, si verificano gli eventi seguenti:

-   La richiesta di I/O viene intercettata da un [redirector di rete](network-redirectors.md), detto anche semplicemente redirector, nel computer locale. Questa operazione viene illustrata nella figura precedente mediante la freccia a tinta unita tra l'applicazione e il redirector client.
-   Il redirector costruisce un pacchetto di dati contenente tutte le informazioni sulla richiesta e lo invia al server in cui si trova il file. Questa operazione viene illustrata nella figura precedente mediante la freccia a tinta unita tra il redirector client e il redirector del server.
-   Il redirector sul server riceve il pacchetto dal client, autentica l'accesso al file richiesto dalla richiesta di I/O e, se autenticato, esegue la richiesta per conto del client. In caso contrario, restituisce un codice di errore al redirector sul client. Questa operazione viene illustrata nella figura precedente mediante la freccia a tinta unita curva tra il redirector del server e il file.
-   Quando la richiesta è stata eseguita, il redirector sul server invia tutti i dati risultanti dalla richiesta di I/O al redirector sul client insieme a una notifica di esito positivo. Questa operazione viene illustrata nella figura precedente dalla freccia tratteggiata tra il server e il redirector client.
-   Il redirector sul client riceve il pacchetto dal server e passa i dati nel pacchetto all'applicazione insieme a una notifica di esito positivo. Questa operazione viene illustrata nella figura precedente dalla freccia tratteggiata tra il redirector client e l'applicazione.

Windows può utilizzare un'ampia gamma di protocolli di rete per eseguire un'operazione di I/O di rete, tra cui il protocollo [Microsoft SMB e la panoramica del protocollo CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) e NFS.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                       | Descrizione                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Differenze nell'I/O locale e di rete](differences-in-local-and-network-i-o.md)<br/> | Differenze tra l'i/o locale e l'I/O di rete in Windows.<br/> |
| [Redirector di rete](network-redirectors.md)<br/>                                   | Descrive la funzionalità di un redirector di rete.<br/>      |



 

 

 




