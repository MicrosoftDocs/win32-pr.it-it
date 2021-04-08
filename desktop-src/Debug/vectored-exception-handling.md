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
# <a name="vectored-exception-handling"></a>Gestione delle eccezioni con vettori

I gestori di eccezioni con vettori sono un'estensione della gestione strutturata delle eccezioni. Un'applicazione può registrare una funzione per controllare o gestire tutte le eccezioni per l'applicazione. I gestori con vettori non sono basati su frame, pertanto è possibile aggiungere un gestore che verrà chiamato indipendentemente dalla posizione in cui si trova il frame di chiamata. I gestori con vettori vengono chiamati nell'ordine in cui sono stati aggiunti, dopo che il debugger ha ottenuto una notifica di prima possibilità, ma prima che il sistema inizi a rimuovere lo stack.

Per aggiungere un gestore di continuazione vettoriale, usare la funzione [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) . Per rimuovere questo gestore, utilizzare la funzione [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .

Per aggiungere un gestore di eccezioni con vettori, utilizzare la funzione [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) . Per rimuovere questo gestore, utilizzare la funzione [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .

 

 
