---
description: Gestione degli errori in WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Gestione degli errori in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72dac7775934684afe6cc9c9d54bc36bb8f3295c91deef7449e9a00600bc687e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899187"
---
# <a name="error-handling-in-winhttp"></a>Gestione degli errori in WinHTTP

Non tutte le funzioni dell'API WinHTTP segnalano gli errori nello stesso modo.

Alcune funzioni, ad esempio [**WinHttpSetTimeouts,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)restituiscono **un valore BOOL** che indica un errore quando **FALSE**. Se **viene restituito FALSE,** i chiamanti interessati all'errore devono chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **GetLastError** viene chiamato quando la funzione è riuscita (ha restituito qualsiasi valore tranne **FALSE),** il valore restituito è imprevedibile e può variare tra le versioni di Windows, i Service Pack o anche tra le chiamate alla stessa funzione.

Alcune funzioni, ad esempio [**WinHttpConnect,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)restituiscono uno pseudo handle [HINTERNET.](hinternet-handles-in-winhttp.md) Queste funzioni sono esattamente le stesse, ad eccezione del fatto che l'errore è indicato dalla restituzione di **NULL.** Se **viene restituito NULL,** i chiamanti interessati all'errore devono chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **GetLastError** viene chiamato quando la funzione ha restituito qualsiasi valore diverso da **NULL,** il valore restituito è imprevedibile e può variare tra le versioni di Windows, i Service Pack o anche tra le chiamate alla stessa funzione.

Alcune funzioni, ad esempio [**WinHttpGetProxyResult,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)restituiscono un codice di errore **DWORD** e non è necessario chiamare altre funzioni per altre informazioni sull'errore. Per queste funzioni, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) non deve essere chiamato. Se **viene chiamato GetLastError,** indipendentemente dall'esito positivo o negativo della funzione, il valore restituito è imprevedibile e può variare tra le versioni di Windows, i Service Pack o anche tra le chiamate alla stessa funzione.

 

 
