---
description: Un handle di socket può facoltativamente essere un handle di file in Windows Sockets 2. Un handle di socket da un provider Winsock può essere usato con altre funzioni non Winsock, ad esempio ReadFile, WriteFile, ReadFileEx e WriteFileEx.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Handle di socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a9c9c642c317e9ab4ef897a20b68184df2c04324bcb76c33dea762e78c2846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740035"
---
# <a name="socket-handles"></a>Handle di socket

Un handle di socket può facoltativamente essere un handle di file in Windows Sockets 2. Un handle di socket da un provider Winsock può essere usato con altre funzioni non Winsock, ad esempio [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)e [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex).

Il **membro \_ IFS \_ HANDLES XP1** nella struttura delle informazioni sul protocollo per un provider determina se un handle socket da un provider è un handle IFS (Installable File System). Gli handle di socket che sono handle IFS possono essere usati senza una penalità delle prestazioni con altre funzioni non Winsock , ad esempio [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e [**WriteFile.**](/windows/win32/api/fileapi/nf-fileapi-writefile) Eventuali handle di socket non IFS quando vengono usati con funzioni non Winsock (ad esempio **ReadFile** e **WriteFile)** comportano interazioni tra il provider e il file system in cui è necessario un sovraccarico di elaborazione aggiuntivo che può comportare una riduzione significativa delle prestazioni. Quando si usano handle socket con funzioni non Winsock, i codici di errore propagati dal file system di base non vengono sempre mappati ai codici di errore Winsock. Di conseguenza, è consigliabile usare gli handle di socket solo con le funzioni Winsock.

Un handle socket non deve essere usato con la [**funzione DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) La presenza di provider di servizi a livelli (LSP) può causare un errore e il processo di destinazione non può importare l'handle del socket.

> [!Note]  
> I provider di servizi su più livelli sono deprecati. A partire da Windows 8 e Windows Server 2012, usare [Windows Filtering Platform.](../fwp/windows-filtering-platform-start-page.md)

 

Windows Sockets 2 ha espanso alcune funzioni che trasferiscono dati tra socket usando handle. Le funzioni offrono vantaggi specifici dei socket per il trasferimento dei dati e [**includono WSARecv,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSADuplicateSocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa)

 

 
