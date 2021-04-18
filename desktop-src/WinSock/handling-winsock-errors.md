---
description: Gestione degli errori in Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Gestione degli errori Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306955"
---
# <a name="handling-winsock-errors"></a>Gestione degli errori Winsock

La maggior parte delle funzioni di Windows Sockets 2 non restituisce la determinata origine di un errore quando la funzione restituisce. Alcune funzioni Winsock restituiscono un valore pari a zero in caso di esito positivo. In caso contrario, \_ viene restituito l'errore di socket del valore (-1) ed è possibile recuperare un numero di errore specifico chiamando la funzione [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Per le funzioni Winsock che restituiscono un handle, un valore restituito di socket non valido \_ (0xFFFF) indica un errore e un numero di errore specifico può essere recuperato chiamando **WSAGetLastError**. Per le funzioni Winsock che restituiscono un puntatore, un valore restituito **null** indica un errore e un numero di errore specifico può essere recuperato chiamando la funzione **WSAGetLastError** .

Un codice di errore Winsock può essere convertito in un valore HRESULT da utilizzare in una chiamata di procedura remota (RPC) utilizzando HRESULT \_ da \_ Win32. Nelle versioni precedenti di Platform Software Development Kit (SDK), HRESULT \_ da \_ Win32 è stato definito come una macro nel file di intestazione *Winerror. h* . Nel Software Development Kit (SDK) di Microsoft Windows, HRESULT \_ da \_ Win32 viene definito come funzione inline nel file di intestazione *Winerror. h* .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici di errore di Windows Sockets](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



