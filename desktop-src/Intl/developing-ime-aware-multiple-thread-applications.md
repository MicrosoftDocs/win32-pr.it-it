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
# <a name="developing-ime-aware-multiple-thread-applications"></a><span data-ttu-id="76e3b-103">Sviluppo di applicazioni con più thread IME-Aware</span><span class="sxs-lookup"><span data-stu-id="76e3b-103">Developing IME-Aware Multiple-thread Applications</span></span>

<span data-ttu-id="76e3b-104">IMM include il controllo di identificazione dei thread che determina se un thread chiamante è il creatore di un handle del contesto del metodo di input specificato (tipo HIMC) o un handle di finestra (tipo HWND).</span><span class="sxs-lookup"><span data-stu-id="76e3b-104">The IMM includes thread identification checking that determines if a calling thread is the creator of a specified input method context handle (HIMC type) or window handle (HWND type).</span></span> <span data-ttu-id="76e3b-105">Se il thread non è il creatore dell'handle, la funzione IMM chiamata ha esito negativo e una chiamata successiva a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ accesso non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="76e3b-105">If the thread is not the creator of the handle, the called IMM function fails and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_ACCESS.</span></span>

> [!Note]  
> <span data-ttu-id="76e3b-106">L'architettura di IMM corrente non fornisce una funzionalità di sincronizzazione per l'accesso agli handle di IMM.</span><span class="sxs-lookup"><span data-stu-id="76e3b-106">The current IMM architecture does not provide a synchronization facility for access to IMM handles.</span></span>

 

<span data-ttu-id="76e3b-107">Per usare il controllo dell'identificazione dei thread, le applicazioni devono rispettare le linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="76e3b-107">To use thread identification checking, your applications must adhere to the following guidelines:</span></span>

-   <span data-ttu-id="76e3b-108">Un thread non deve accedere al contesto di input creato da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="76e3b-108">A thread should not access the input context created by another thread.</span></span>
-   <span data-ttu-id="76e3b-109">Un thread non deve associare un contesto di input a una finestra creata da un altro thread e viceversa.</span><span class="sxs-lookup"><span data-stu-id="76e3b-109">A thread should not associate an input context with a window created by another thread, and vice versa.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76e3b-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76e3b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76e3b-111">Uso di gestione metodi di input</span><span class="sxs-lookup"><span data-stu-id="76e3b-111">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
