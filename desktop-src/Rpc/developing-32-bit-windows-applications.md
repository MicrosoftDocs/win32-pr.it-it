---
title: Sviluppo di applicazioni Windows RPC
description: Quando si installa Platform Software Development Kit (SDK), l'ambiente di sviluppo RPC seguente, le librerie di runtime e gli strumenti vengono installati automaticamente
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047251"
---
# <a name="developing-rpc-windows-applications"></a>Sviluppo di applicazioni Windows RPC

Quando si installa Platform Software Development Kit (SDK), l'ambiente di sviluppo RPC seguente, le librerie di runtime e gli strumenti vengono installati automaticamente:

-   Intestazione del linguaggio C/C++ (. File H)
-   File delle librerie di importazione RPC (lib)
-   Programmi di esempio
-   File della Guida di riferimento RPC
-   Utilità **uuidgen**

Quando si installa Windows, vengono installati i seguenti elementi:

-   Dll di runtime RPC
-   Microsoft Locator (non supportato in Windows Vista e versioni successive)
-   Servizi di mapping degli endpoint RPC

Librerie di importazione RPC seguenti.



| Libreria di importazione | Descrizione                |
|----------------|----------------------------|
| Rpcns4. lib     | Nome-funzioni servizio     |
| Rpcrt4. lib     | Funzioni di runtime di Windows |



 

> [!Note]  
> Rpcns4. lib è obsoleto e non è più supportato.

 

Per il supporto di livello inferiore sono incluse le librerie RPC seguenti.



| Libreria a collegamento dinamico | Descrizione                 | Piattaforma                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Trasporto named pipe del client | Windows NT, Windows 98, Windows 95 |
| Rpclts1.dll          | Trasporto named pipe del server | Windows NT, Windows 98, Windows 95 |
| Rpcltc3.dll          | Trasporto TCP/IP client     | Windows NT, Windows 98, Windows 95 |
| Rpclts3.dll          | Trasporto TCP/IP del server     | Windows NT, Windows 98, Windows 95 |
| Rpcltc5.dll          | Trasporto NetBIOS client    | Windows NT, Windows 98, Windows 95 |
| Rpclts5.dll          | Trasporto NetBIOS server    | Windows NT, Windows 98, Windows 95 |
| Rpcltc6.dll          | Trasporto SPX client        | Windows NT, Windows 98, Windows 95 |
| Rpclts6.dll          | Trasporto SPX server        | Windows NT, Windows 98, Windows 95 |
| Rpcdgc6.dll          | Trasporto IPX client        | Windows NT                         |
| Rpcdgs6.dll          | Trasporto IPX server        | Windows NT                         |
| Rpcdgc3.dll          | Trasporto UDP client        | Windows NT                         |
| Rpcdgs3.dll          | Trasporto UDP del server        | Windows NT                         |



 

Sarà inoltre necessario il compilatore Microsoft Interface Definition Language (MIDL). Per altre informazioni, vedere [uso del compilatore MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).

 

 