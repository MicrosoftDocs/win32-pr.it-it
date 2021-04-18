---
description: IMM include il controllo di identificazione dei thread che determina se un thread chiamante è il creatore di un handle del contesto del metodo di input specificato (tipo HIMC) o un handle di finestra (tipo HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Sviluppo di applicazioni con più thread IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317172"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>Sviluppo di applicazioni con più thread IME-Aware

IMM include il controllo di identificazione dei thread che determina se un thread chiamante è il creatore di un handle del contesto del metodo di input specificato (tipo HIMC) o un handle di finestra (tipo HWND). Se il thread non è il creatore dell'handle, la funzione IMM chiamata ha esito negativo e una chiamata successiva a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ accesso non valido \_ .

> [!Note]  
> L'architettura di IMM corrente non fornisce una funzionalità di sincronizzazione per l'accesso agli handle di IMM.

 

Per usare il controllo dell'identificazione dei thread, le applicazioni devono rispettare le linee guida seguenti:

-   Un thread non deve accedere al contesto di input creato da un altro thread.
-   Un thread non deve associare un contesto di input a una finestra creata da un altro thread e viceversa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di gestione metodi di input](using-input-method-manager.md)
</dt> </dl>

 

 
