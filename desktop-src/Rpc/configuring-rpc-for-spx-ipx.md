---
title: Configurazione di RPC per SPX/IPX
description: Quando si usano i \_ trasporti IPX ncacn SPX e ncadg \_ , il nome del server è esattamente uguale al nome del server in Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471507"
---
# <a name="configuring-rpc-for-spxipx"></a>Configurazione di RPC per SPX/IPX

Quando si usano i trasporti **\_ IPX** **ncacn \_ SPX** e ncadg, il nome del server è esattamente uguale al nome del server in Windows. Tuttavia, poiché i nomi vengono distribuiti usando i protocolli Novell, devono essere conformi alle convenzioni di denominazione Novell. Se il nome di un server non è un nome Novell valido, i server non saranno in grado di creare endpoint con i trasporti **\_ IPX** **ncacn \_ SPX** o ncadg.

Un nome di server Novell valido contiene solo i caratteri compresi tra 0x20 e 0x7F. I caratteri minuscoli vengono modificati in maiuscolo. Non è possibile usare i caratteri seguenti:

" \* ,./:; <=>?\[\]\\\|\]

Per mantenere la compatibilità con la prima versione di Windows NT, **ncacn \_ SPX** e **ncadg \_ IPX** consentono anche di usare un formato speciale del nome del server noto come nome tilde. Il nome della tilde è costituito da una tilde (~), seguita dal numero di rete di otto cifre del server e quindi da un indirizzo Ethernet a 12 cifre. I nomi tilde hanno un vantaggio nel fatto che non richiedono funzionalità di servizio dei nomi. Pertanto, se si è connessi a un server, il nome della tilde funzionerà.

Le tabelle seguenti contengono due configurazioni di esempio che illustrano i punti descritti in precedenza.



| Componente                            | Configurato come      |
|--------------------------------------|--------------------|
| Windows Server                       | NWCS               |
| Client Windows                       | NWCS               |
| client Windows a 16 bit, client MS-DOS | Redirector NetWare |



 

Per la configurazione nella tabella precedente è necessario che nella rete siano presenti file server o router NetWare. In quanto i nomi dei server vengono archiviati nell'associazione NetWare.



| Componente                            | Configurato come |
|--------------------------------------|---------------|
| Windows Server                       | Agente SAP     |
| Client Windows                       | IPX/SPX       |
| client Windows a 16 bit, client MS-DOS | IPX/SPX       |



 

La seconda configurazione funziona in un ambiente che non contiene file server o router NetWare, ad esempio una rete di due computer: un server Windows e un client MS-DOS. La risoluzione dei nomi, eseguita durante la prima chiamata su un handle di binding, sarà leggermente più lenta rispetto alla prima configurazione. Inoltre, la seconda configurazione comporta un maggiore traffico generato sulla rete.

Per implementare la risoluzione dei nomi, quando un server RPC utilizza un endpoint SPX o IPX, il nome del server e l'endpoint vengono registrati come Server Service Advertising Protocol (SAP) di tipo 640 (esadecimale). Per risolvere il nome di un server, il client RPC invia una richiesta SAP per tutti i servizi dello stesso tipo e quindi analizza l'elenco di risposte per il nome del server. Questo processo si verifica durante la prima chiamata RPC su ogni handle di binding. Per ulteriori informazioni sul protocollo SAP per Novell, vedere la documentazione di NetWare.

> [!Note]  
> Le applicazioni client Windows a 16 bit che usano i trasporti **\_ IPX** **ncacn \_ SPX** o ncadg richiedono che il file Nwipxspx.dll sia installato per l'esecuzione nel sottosistema WOW. Per ottenere questo file, contattare Novell.

 

 

 




