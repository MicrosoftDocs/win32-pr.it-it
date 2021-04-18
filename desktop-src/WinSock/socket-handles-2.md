---
description: Un handle di socket può facoltativamente essere un handle di file in Windows Sockets 2. È possibile utilizzare un handle di socket da un provider Winsock con altre funzioni non Winsock, ad esempio ReadFile, WriteFile, ReadFileEx e WriteFileEx.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Handle socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6ca8ed935819e018a59c52fb43dcf816530c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310425"
---
# <a name="socket-handles"></a>Handle socket

Un handle di socket può facoltativamente essere un handle di file in Windows Sockets 2. È possibile utilizzare un handle di socket da un provider Winsock con altre funzioni non Winsock, ad esempio [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)e [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex).

Il **XP1 \_ IFS \_ gestisce** il membro nella struttura delle informazioni di protocollo per un provider determina se un handle di socket da un provider è un handle di file system installabile (IFS). Gli handle di socket che sono handle IFS possono essere usati senza una riduzione delle prestazioni con altre funzioni non Winsock (ad esempio,[**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile)). Tutti gli handle non IFS socket se usati con funzioni non Winsock (ad esempio,**ReadFile** e **WriteFile**) comportano interazioni tra il provider e il file System in cui è presente un sovraccarico di elaborazione aggiuntivo che può comportare una riduzione significativa delle prestazioni. Quando si utilizzano handle di socket con funzioni non Winsock, i codici di errore propagati dal file system di base non sono sempre mappati ai codici di errore Winsock. Di conseguenza, è consigliabile utilizzare gli handle di socket solo con le funzioni Winsock.

Non usare un handle di socket con la funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) . La presenza di provider di servizi su più livelli (LSP) può causare un errore e non esiste alcun modo per il processo di destinazione di importare l'handle del socket.

> [!Note]  
> I provider di servizi sovrapposti sono deprecati. A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

Windows Sockets 2 ha espanso alcune funzioni che trasferiscono i dati tra i socket usando gli handle. Le funzioni offrono vantaggi specifici dei socket per il trasferimento di dati e includono [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa).

 

 
