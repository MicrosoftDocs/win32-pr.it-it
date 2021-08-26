---
title: Configurazione di RPC per SPX/IPX
description: Quando si usano i trasporti ncacn spx e \_ ncadg ipx, il nome del server corrisponde esattamente al nome \_ del server in Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5557541b296c436f2c3c1de007eb0e331e1c77d0529be83e758a25b76ac5e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022451"
---
# <a name="configuring-rpc-for-spxipx"></a>Configurazione di RPC per SPX/IPX

Quando si usano i trasporti **ncacn \_ spx** e **ncadg \_ ipx,** il nome del server corrisponde esattamente al nome del server in Windows. Tuttavia, poiché i nomi vengono distribuiti usando protocolli Novell, devono essere conformi alle convenzioni di denominazione di Novell. Se un nome di server non è un nome Novell valido, i server non saranno in grado di creare endpoint con i trasporti **ncacn \_ spx** **o ncadg \_ ipx.**

Un nome di server Novell valido contiene solo i caratteri compresi tra 0x20 e 0x7f. I caratteri minuscoli vengono modificati in maiuscolo. Non è possibile usare i caratteri seguenti:

" \* ,./:;<=>?\[\]\\\|\]

Per mantenere la compatibilità con la prima versione di Windows NT, **ncacn \_ spx** e **ncadg \_ ipx** consentono anche di usare un formato speciale del nome del server noto come nome tilde. Il nome della tilde è costituito da una tilde (~), seguita dal numero di rete a otto cifre del server e quindi dal relativo indirizzo Ethernet a 12 cifre. I nomi tilde hanno un vantaggio in quanto non richiedono alcuna funzionalità del servizio dei nomi. Pertanto, se si è connessi a un server, il nome tilde funzionerà.

Le tabelle seguenti contengono due configurazioni di esempio che illustrano i punti descritti in precedenza.



| Componente                            | Configurato come      |
|--------------------------------------|--------------------|
| Windows Server                       | NWCS               |
| Client Windows                       | NWCS               |
| Client Windows a 16 bit, client MS-DOS | NetWare Redirector |



 

Per la configurazione nella tabella precedente è necessario disporre di file server o router NetWare nella rete. Produce prestazioni ottimali perché i nomi dei server vengono archiviati nel bindery NetWare.



| Componente                            | Configurato come |
|--------------------------------------|---------------|
| Windows Server                       | Agente SAP     |
| Client Windows                       | IPX/SPX       |
| Client Windows a 16 bit, client MS-DOS | IPX/SPX       |



 

La seconda configurazione funziona in un ambiente che non contiene file server o router NetWare(ad esempio, una rete di due computer: un server Windows e un client MS-DOS). La risoluzione dei nomi, eseguita durante la prima chiamata su un handle di associazione, sarà leggermente più lenta rispetto alla prima configurazione. Inoltre, la seconda configurazione comporta un maggiore traffico generato in rete.

Per implementare la risoluzione dei nomi, quando un server RPC usa un endpoint SPX o IPX, il nome del server e l'endpoint vengono registrati come server Service Advertising Protocol (SAP) di tipo 640 (esadecimale). Per risolvere un nome di server, il client RPC invia una richiesta SAP per tutti i servizi dello stesso tipo e quindi analizza l'elenco di risposte per il nome del server. Questo processo si verifica durante la prima chiamata RPC su ogni handle di associazione. Per altre informazioni sul protocollo SAP per Novell, vedere la documentazione di NetWare.

> [!Note]  
> Le applicazioni client Windows a 16 bit che usano i trasporti **ncacn \_ spx** o **ncadg \_ ipx** richiedono l'installazione del Nwipxspx.dll file per l'esecuzione nel sottosistema WOW. Per ottenere questo file, contattare Novell.

 

 

 




