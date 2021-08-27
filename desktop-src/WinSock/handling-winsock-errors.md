---
description: Gestione degli errori in Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Gestione degli errori Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbb0ea47fc023ce0d6ae47f82a6bb9d732e052d5749fe58f9a405d6784d941b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097901"
---
# <a name="handling-winsock-errors"></a>Gestione degli errori Winsock

La Windows socket 2 non restituisce la causa specifica di un errore quando la funzione restituisce . Alcune funzioni Winsock restituiscono un valore pari a zero in caso di esito positivo. In caso contrario, viene restituito il valore SOCKET ERROR (-1) e un numero di errore specifico può essere recuperato chiamando \_ la [**funzione WSAGetLastError.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) Per le funzioni Winsock che restituiscono un handle, un valore restituito INVALID SOCKET (0xffff) indica un errore e un numero di errore specifico può essere recuperato chiamando \_ **WSAGetLastError**. Per le funzioni Winsock che restituiscono un puntatore, un valore restituito **NULL** indica un errore e un numero di errore specifico può essere recuperato chiamando la **funzione WSAGetLastError.**

Un codice di errore Winsock può essere convertito in HRESULT per l'uso in una chiamata di procedura remota (RPC) tramite HRESULT \_ FROM \_ WIN32. Nelle versioni precedenti di Platform Software Development Kit (SDK), HRESULT FROM WIN32 è stato definito come macro nel file di \_ \_ intestazione *Winerror.h.* In Microsoft Windows Software Development Kit (SDK), HRESULT FROM WIN32 è definito come funzione inline nel \_ \_ file di intestazione *Winerror.h.*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Codici di errore dei socket](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



