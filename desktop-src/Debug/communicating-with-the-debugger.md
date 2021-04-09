---
description: La funzione OutputDebugString invia una stringa dal processo sottoposto a debug al debugger generando un evento di debug degli eventi di stringa di debug di OUTPUT \_ \_ \_ . Un processo può rilevare se è in fase di debug chiamando la funzione IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Comunicazione con il debugger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877177"
---
# <a name="communicating-with-the-debugger"></a>Comunicazione con il debugger

La funzione [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) invia una stringa dal processo sottoposto a debug al debugger generando un evento di debug degli eventi di stringa di debug di output \_ \_ \_ . Un processo può rilevare se è in fase di debug chiamando la funzione [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .

La funzione [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) causa un'eccezione del punto di interruzione nel processo corrente. Un punto di interruzione è un percorso in un programma in cui l'esecuzione viene arrestata per consentire allo sviluppatore di esaminare il codice, le variabili e i valori di registrazione del programma e, in base alle esigenze, di apportare modifiche, continuare l'esecuzione o terminare l'esecuzione.

La funzione [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) termina il processo corrente e fornisce il controllo di esecuzione al debugger, ma a differenza di [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), non genera un'eccezione. Questa funzione deve essere usata solo come ultima risorsa, perché non sempre libera la memoria del processo o chiude i relativi file.

 

 
