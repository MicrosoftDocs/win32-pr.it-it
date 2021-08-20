---
description: I gestori di eccezioni vettoriali sono un'estensione alla gestione strutturata delle eccezioni.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Gestione delle eccezioni vettoriali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926b0499e9399aa77e6835e90c6da016da3f2dc8195a4b4872f7f5119d04978a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405582"
---
# <a name="vectored-exception-handling"></a>Gestione delle eccezioni vettoriali

I gestori di eccezioni vettoriali sono un'estensione alla gestione strutturata delle eccezioni. Un'applicazione può registrare una funzione per controllare o gestire tutte le eccezioni per l'applicazione. I gestori vettoriali non sono basati su frame, pertanto è possibile aggiungere un gestore che verrà chiamato indipendentemente dalla posizione in cui ci si trova in un frame di chiamata. I gestori vettoriali vengono chiamati nell'ordine in cui sono stati aggiunti, dopo che il debugger ottiene una notifica first chance, ma prima che il sistema inizi la rimozione dello stack.

Per aggiungere un gestore di continuazione vettoriale, usare [**la funzione AddVectoredContinueHandler.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) Per rimuovere questo gestore, usare [**la funzione RemoveVectoredContinueHandler.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

Per aggiungere un gestore di eccezioni vettoriali, usare [**la funzione AddVectoredExceptionHandler.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) Per rimuovere questo gestore, usare [**la funzione RemoveVectoredExceptionHandler.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

 

 
