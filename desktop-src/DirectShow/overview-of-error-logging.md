---
description: Panoramica della registrazione degli errori
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Panoramica della registrazione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124368"
---
# <a name="overview-of-error-logging"></a><span data-ttu-id="07a2a-103">Panoramica della registrazione degli errori</span><span class="sxs-lookup"><span data-stu-id="07a2a-103">Overview of Error Logging</span></span>

<span data-ttu-id="07a2a-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="07a2a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="07a2a-105">Per garantire la massima flessibilità per le applicazioni nella gestione degli errori, i [servizi di modifica DirectShow](directshow-editing-services.md) utilizzano un meccanismo di callback.</span><span class="sxs-lookup"><span data-stu-id="07a2a-105">To give applications maximum flexibility in handling errors, [DirectShow Editing Services](directshow-editing-services.md) uses a callback mechanism.</span></span> <span data-ttu-id="07a2a-106">L'applicazione implementa un metodo per la registrazione di un errore.</span><span class="sxs-lookup"><span data-stu-id="07a2a-106">Your application implements a method for logging an error.</span></span> <span data-ttu-id="07a2a-107">In fase di esecuzione, se si verifica un errore, DES chiama il metodo fornito.</span><span class="sxs-lookup"><span data-stu-id="07a2a-107">At run time, if an error occurs, DES calls the method you have provided.</span></span> <span data-ttu-id="07a2a-108">Il metodo accetta parametri che descrivono l'errore.</span><span class="sxs-lookup"><span data-stu-id="07a2a-108">The method takes parameters that describe the error.</span></span> <span data-ttu-id="07a2a-109">L'operazione eseguita dal metodo con queste informazioni dipende dall'utente.</span><span class="sxs-lookup"><span data-stu-id="07a2a-109">What the method does with this information is up to you.</span></span> <span data-ttu-id="07a2a-110">(Deve essere restituito il più rapidamente possibile, tuttavia, oppure potrebbe interferire con l'esecuzione del programma).</span><span class="sxs-lookup"><span data-stu-id="07a2a-110">(It should return as quickly as possible, however, or it might interfere with the execution of the program.)</span></span>

<span data-ttu-id="07a2a-111">Il metodo di callback per la registrazione degli errori è contenuto in un'interfaccia COM, [**IAMErrorLog**](iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="07a2a-111">The error logging callback method is contained in a COM interface, [**IAMErrorLog**](iamerrorlog.md).</span></span> <span data-ttu-id="07a2a-112">L'applicazione deve implementare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="07a2a-112">Your application must implement this interface.</span></span> <span data-ttu-id="07a2a-113">Come tutte le interfacce COM, **IAMErrorLog** eredita l'interfaccia **IUnknown** , quindi l'applicazione deve implementare anche tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="07a2a-113">Like all COM interfaces, **IAMErrorLog** inherits the **IUnknown** interface, so your application must implement that as well.</span></span>

<span data-ttu-id="07a2a-114">Sono disponibili diverse opzioni per l'implementazione di queste interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="07a2a-114">You have several choices for implementing these COM interfaces.</span></span> <span data-ttu-id="07a2a-115">È possibile utilizzare il Active Template Library (ATL), che fornisce le implementazioni predefinite dei metodi **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="07a2a-115">You can use the Active Template Library (ATL), which provides stock implementations of the **IUnknown** methods.</span></span> <span data-ttu-id="07a2a-116">DirectShow fornisce anche una classe base C++, [**CUnknown**](cunknown.md), che semplifica l'implementazione di un'interfaccia com.</span><span class="sxs-lookup"><span data-stu-id="07a2a-116">DirectShow also provides a C++ base class, [**CUnknown**](cunknown.md), that makes it easy to implement a COM interface.</span></span> <span data-ttu-id="07a2a-117">Per informazioni sull'uso di **CUnknown**, vedere [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="07a2a-117">For information on using **CUnknown**, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

<span data-ttu-id="07a2a-118">Il codice di esempio in questo articolo definisce una classe C++ autonoma che implementa sia **IUnknown** che **IAMErrorLog**.</span><span class="sxs-lookup"><span data-stu-id="07a2a-118">The sample code in this article defines a self-contained C++ class, which implements both **IUnknown** and **IAMErrorLog**.</span></span> <span data-ttu-id="07a2a-119">Il risultato non è un vero oggetto COM, perché non supporta **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="07a2a-119">The result is not a true COM object, because it does not support **CoCreateInstance**.</span></span> <span data-ttu-id="07a2a-120">Tuttavia, questo approccio è adeguato ai fini dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="07a2a-120">However, this approach is adequate for the purpose of the example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07a2a-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07a2a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a2a-122">Errori di registrazione</span><span class="sxs-lookup"><span data-stu-id="07a2a-122">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



