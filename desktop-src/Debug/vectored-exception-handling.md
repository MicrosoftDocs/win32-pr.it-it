---
description: I gestori di eccezioni con vettori sono un'estensione della gestione strutturata delle eccezioni.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Gestione delle eccezioni con vettori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877770"
---
# <a name="vectored-exception-handling"></a><span data-ttu-id="8ecfe-103">Gestione delle eccezioni con vettori</span><span class="sxs-lookup"><span data-stu-id="8ecfe-103">Vectored Exception Handling</span></span>

<span data-ttu-id="8ecfe-104">I gestori di eccezioni con vettori sono un'estensione della gestione strutturata delle eccezioni.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-104">Vectored exception handlers are an extension to structured exception handling.</span></span> <span data-ttu-id="8ecfe-105">Un'applicazione può registrare una funzione per controllare o gestire tutte le eccezioni per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-105">An application can register a function to watch or handle all exceptions for the application.</span></span> <span data-ttu-id="8ecfe-106">I gestori con vettori non sono basati su frame, pertanto è possibile aggiungere un gestore che verrà chiamato indipendentemente dalla posizione in cui si trova il frame di chiamata.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-106">Vectored handlers are not frame-based, therefore, you can add a handler that will be called regardless of where you are in a call frame.</span></span> <span data-ttu-id="8ecfe-107">I gestori con vettori vengono chiamati nell'ordine in cui sono stati aggiunti, dopo che il debugger ha ottenuto una notifica di prima possibilità, ma prima che il sistema inizi a rimuovere lo stack.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-107">Vectored handlers are called in the order that they were added, after the debugger gets a first chance notification, but before the system begins unwinding the stack.</span></span>

<span data-ttu-id="8ecfe-108">Per aggiungere un gestore di continuazione vettoriale, usare la funzione [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="8ecfe-108">To add a vectored continue handler, use the [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) function.</span></span> <span data-ttu-id="8ecfe-109">Per rimuovere questo gestore, utilizzare la funzione [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="8ecfe-109">To remove this handler, use the [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) function.</span></span>

<span data-ttu-id="8ecfe-110">Per aggiungere un gestore di eccezioni con vettori, utilizzare la funzione [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="8ecfe-110">To add a vectored exception handler, use the [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) function.</span></span> <span data-ttu-id="8ecfe-111">Per rimuovere questo gestore, utilizzare la funzione [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="8ecfe-111">To remove this handler, use the [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) function.</span></span>

 

 
