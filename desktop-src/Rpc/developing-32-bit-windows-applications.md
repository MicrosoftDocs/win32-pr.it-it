---
title: Sviluppo di applicazioni Windows RPC
description: Quando si installa Platform Software Development Kit (SDK), vengono installati automaticamente l'ambiente di sviluppo RPC, le librerie di runtime e gli strumenti seguenti
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ddb48a38faadb8235064fa735fa8a75a80a62308990373ab1971d4a6cd9ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930796"
---
# <a name="developing-rpc-windows-applications"></a>Sviluppo di applicazioni Windows RPC

Quando si installa Platform Software Development Kit (SDK), vengono installati automaticamente l'ambiente di sviluppo RPC, le librerie di runtime e gli strumenti seguenti:

-   Intestazione del linguaggio C/C++ (. H) file
-   File di librerie di importazione RPC (con estensione lib)
-   Programmi di esempio
-   File della Guida di riferimento RPC
-   Utilità **uuidgen**

Quando si installa Windows, vengono installati gli elementi seguenti:

-   DLL di run-time RPC
-   Microsoft Locator (non supportato in Windows Vista e versioni successive)
-   Servizi di mapping degli endpoint RPC

Le librerie di importazione RPC seguenti.



| Importare la libreria | Descrizione                |
|----------------|----------------------------|
| Rpcns4.lib     | Funzioni del servizio dei nomi     |
| Rpcrt4.lib     | Windows funzioni di run-time |



 

> [!Note]  
> Rpcns4.lib è obsoleto e non è più supportato.

 

Le librerie RPC seguenti sono incluse per il supporto di livello inferiore.



| Libreria a collegamento dinamico | Descrizione                 | Piattaforma                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Trasporto named pipe client | Windows NT, Windows 98, Windows 95 |
| Rpclts1.dll          | Trasporto named pipe del server | Windows NT, Windows 98, Windows 95 |
| Rpcltc3.dll          | Trasporto TCP/IP client     | Windows NT, Windows 98, Windows 95 |
| Rpclts3.dll          | Trasporto TCP/IP del server     | Windows NT, Windows 98, Windows 95 |
| Rpcltc5.dll          | Trasporto NetBIOS client    | Windows NT, Windows 98, Windows 95 |
| Rpclts5.dll          | Trasporto NetBIOS del server    | Windows NT, Windows 98, Windows 95 |
| Rpcltc6.dll          | Trasporto SPX client        | Windows NT, Windows 98, Windows 95 |
| Rpclts6.dll          | Trasporto SPX del server        | Windows NT, Windows 98, Windows 95 |
| Rpcdgc6.dll          | Trasporto IPX client        | Windows NT                         |
| Rpcdgs6.dll          | Trasporto IPX del server        | Windows NT                         |
| Rpcdgc3.dll          | Trasporto UDP client        | Windows NT                         |
| Rpcdgs3.dll          | Trasporto UDP del server        | Windows NT                         |



 

Sarà necessario anche il compilatore Microsoft Interface Definition Language (MIDL). Per altre informazioni, vedere [Uso del compilatore MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).

 

 