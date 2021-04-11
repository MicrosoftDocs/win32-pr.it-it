---
title: Gestione degli errori degli oggetti servizio
description: Quando si verifica un errore in un oggetto servizio, il valore restituito per la chiamata IDispatch Invoke deve essere DISP \_ E \_ Exception e il puntatore al parametro pExceptInfo a una struttura EXCEPTINFO in deve essere compilato.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd39d08dc7ca5152ca412df1a6fb67d6df524f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117910"
---
# <a name="service-object-error-handling"></a><span data-ttu-id="3877b-103">Gestione degli errori degli oggetti servizio</span><span class="sxs-lookup"><span data-stu-id="3877b-103">Service Object Error Handling</span></span>

<span data-ttu-id="3877b-104">Quando si verifica un errore in un oggetto servizio, il valore restituito per la chiamata [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) deve essere disp \_ e \_ l'eccezione e il puntatore al parametro *pExceptInfo* a una struttura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) in devono essere compilati.</span><span class="sxs-lookup"><span data-stu-id="3877b-104">When an error occurs in a service object, the return value for the call [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) should be DISP\_E\_EXCEPTION, and the *pExceptInfo* parameter pointer to an [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure in the should be filled in.</span></span>

<span data-ttu-id="3877b-105">In particolare, i membri **bstrSource** e **BstrDescription** della struttura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) vengono utilizzati dall'host del dispositivo con la tecnologia UPnP per creare una risposta di errore UPnP. **bstrSource** è il codice di errore e **bstrDescription** è la descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="3877b-105">Specifically, the **bstrSource**, and **bstrDescription** members of the [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure are used by the Device Host with UPnP technology to create a UPnP Fault response; **bstrSource** is the error code and **bstrDescription** is the error description.</span></span>

 

 