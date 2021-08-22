---
description: IMM include il controllo dell'identificazione del thread che determina se un thread chiamante è l'autore di un handle di contesto del metodo di input specificato (tipo HIMC) o handle di finestra (tipo HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Sviluppo IME-Aware applicazioni a thread multipli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf495922d347119db3b8b517af13c850f2f19dfc558609f93f24953f0a3386a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949596"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>Sviluppo IME-Aware applicazioni a thread multipli

IMM include il controllo dell'identificazione del thread che determina se un thread chiamante è l'autore di un handle di contesto del metodo di input specificato (tipo HIMC) o handle di finestra (tipo HWND). Se il thread non è l'autore dell'handle, la funzione IMM chiamata ha esito negativo e una chiamata successiva a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ INVALID \_ ACCESS.

> [!Note]  
> L'architettura IMM corrente non offre una funzionalità di sincronizzazione per l'accesso agli handle IMM.

 

Per usare il controllo dell'identificazione dei thread, le applicazioni devono rispettare le linee guida seguenti:

-   Un thread non deve accedere al contesto di input creato da un altro thread.
-   Un thread non deve associare un contesto di input a una finestra creata da un altro thread e viceversa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Gestione metodi di input](using-input-method-manager.md)
</dt> </dl>

 

 
