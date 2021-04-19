---
description: Gestione degli errori in WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Gestione degli errori in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf234220d0973e86c830063e4ecc25312fa2d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316008"
---
# <a name="error-handling-in-winhttp"></a>Gestione degli errori in WinHTTP

Non tutte le funzioni API WinHTTP segnalano gli errori nello stesso modo.

Alcune funzioni, ad esempio [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts), restituiscono un valore **bool** che indica un errore quando **false**. Se viene restituito **false** , i chiamanti interessati dall'errore devono chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **GetLastError** viene chiamato quando la funzione riuscito (restituisce un valore diverso da **false**), il valore restituito è imprevedibile e può variare tra le versioni di Windows, i Service Pack o anche tra le chiamate alla stessa funzione.

Alcune funzioni, ad esempio [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), restituiscono un handle pseudo [HINTERNET](hinternet-handles-in-winhttp.md) . Queste funzioni sono identiche, ad eccezione del fatto che l'errore viene indicato restituendo **null**. Se viene restituito **null** , i chiamanti interessati dall'errore devono chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **GetLastError** viene chiamato quando la funzione riuscito (restituisce **null**), il valore restituito è imprevedibile e può variare tra le versioni di Windows, i Service Pack o anche tra le chiamate alla stessa funzione.

Alcune funzioni, ad esempio [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult), restituiscono un codice di errore **DWORD** e non è necessario chiamare altre funzioni per ottenere ulteriori informazioni sull'errore. Per queste funzioni, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) non deve essere chiamato. Se **GetLastError** viene chiamato, indipendentemente dall'esito positivo o negativo della funzione, il valore restituito è imprevedibile e può variare tra le versioni di Windows, i Service Pack o anche tra le chiamate alla stessa funzione.

 

 
