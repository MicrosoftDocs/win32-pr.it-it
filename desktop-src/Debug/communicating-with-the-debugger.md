---
description: La funzione OutputDebugString invia una stringa dal processo di cui è in corso il debug al debugger generando un evento di \_ debug OUTPUT DEBUG STRING \_ \_ EVENT. Un processo può rilevare se è in corso il debug chiamando la funzione IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Comunicazione con il debugger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee4d78fc2b0cef1df9f0597a816966585d00e1041711d4712d1a1fa66639e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692061"
---
# <a name="communicating-with-the-debugger"></a>Comunicazione con il debugger

La [**funzione OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) invia una stringa dal processo di cui è in corso il debug al debugger generando un evento di \_ debug OUTPUT DEBUG STRING \_ \_ EVENT. Un processo può rilevare se è in corso il debug chiamando la [**funzione IsDebuggerPresent.**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)

La [**funzione DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) genera un'eccezione del punto di interruzione nel processo corrente. Un punto di interruzione è una posizione in un programma in cui l'esecuzione viene arrestata per consentire allo sviluppatore di esaminare il codice, le variabili e i valori di registrazione del programma e, se necessario, di apportare modifiche, continuare l'esecuzione o terminare l'esecuzione.

La [**funzione FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) termina il processo corrente e fornisce il controllo dell'esecuzione al debugger, ma a differenza di [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), non genera un'eccezione. Questa funzione deve essere usata solo come ultima risorsa, perché non sempre libera la memoria del processo o chiude i file.

 

 
