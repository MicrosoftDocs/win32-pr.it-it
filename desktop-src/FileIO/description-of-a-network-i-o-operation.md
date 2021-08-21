---
description: Descrive il processo di un'operazione di I/O di rete in Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Descrizione di un'operazione di I/O di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d872f8eaf6f9a90ab313e6a7b17e3fe93073cdb13e5b039e401de41287f1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150823"
---
# <a name="description-of-a-network-io-operation"></a>Descrizione di un'operazione di I/O di rete

La figura seguente illustra il processo di un'operazione di I/O di rete in Windows.

![operazione di i/o di rete in Windows](images/fig4.png)

Quando un'applicazione chiama una funzione di I/O di file per accedere a un file in un computer remoto, si verificano gli eventi seguenti:

-   La richiesta di I/O viene intercettata da un [redirector](network-redirectors.md)di rete, detto anche semplicemente redirector, nel computer locale. Questa operazione è illustrata nella figura precedente dalla freccia a tinta unita tra l'applicazione e il redirector client.
-   Il redirector costruisce un pacchetto di dati contenente tutte le informazioni sulla richiesta e lo invia al server in cui si trova il file. Ciò è illustrato nella figura precedente dalla freccia a tinta unita tra il redirector client e il redirector del server.
-   Il redirector nel server riceve il pacchetto dal client, autentica l'accesso al file richiesto dalla richiesta di I/O e, se autenticato, esegue la richiesta per conto del client. In caso contrario, restituisce un codice di errore al redirector nel client. Questa opzione è illustrata nella figura precedente dalla freccia a tinta unita curva tra il redirector del server e il file.
-   Dopo l'esecuzione della richiesta, il redirector sul server invia tutti i dati risultanti dalla richiesta di I/O al redirector nel client insieme a una notifica di esito positivo. Nella figura precedente viene illustrata la freccia punteggiata tra il server e il redirector client.
-   Il redirector nel client riceve il pacchetto dal server e passa i dati nel pacchetto all'applicazione insieme a una notifica di esito positivo. Nella figura precedente viene illustrata la freccia punteggiata tra il redirector client e l'applicazione.

Windows possibile usare un'ampia gamma di protocolli di rete per eseguire un'operazione di I/O di rete, tra cui [Microsoft SMB Protocol e CIFS Protocol Overview](microsoft-smb-protocol-and-cifs-protocol-overview.md) e NFS.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                       | Descrizione                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Differenze nell'I/O locale e di rete](differences-in-local-and-network-i-o.md)<br/> | Differenze tra I/O locale e I/O di rete Windows.<br/> |
| [Redirector di rete](network-redirectors.md)<br/>                                   | Descrive la funzionalità di un redirector di rete.<br/>      |



 

 

 




