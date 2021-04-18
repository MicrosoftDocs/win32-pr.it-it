---
description: Suggerimenti per la risoluzione dei problemi
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Suggerimenti per la risoluzione dei problemi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313401"
---
# <a name="troubleshooting-tips"></a><span data-ttu-id="11276-103">Suggerimenti per la risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="11276-103">Troubleshooting Tips</span></span>

<span data-ttu-id="11276-104">I suggerimenti seguenti consentono di evitare deadlock o arresti anomali dell'applicazione DirectShow.</span><span class="sxs-lookup"><span data-stu-id="11276-104">This following tips will help you to avoid deadlocks or crashes in your DirectShow application.</span></span>

<span data-ttu-id="11276-105">**Oggetti globali**</span><span class="sxs-lookup"><span data-stu-id="11276-105">**Global Objects**</span></span>

<span data-ttu-id="11276-106">Un oggetto C++ globale non deve creare oggetti DirectShow nel metodo del costruttore o rilasciarli nel metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="11276-106">A global C++ object should not create DirectShow objects in its constructor method or release them in its destructor method.</span></span> <span data-ttu-id="11276-107">In questo modo l'applicazione può bloccarsi per un periodo illimitato, per il motivo seguente:</span><span class="sxs-lookup"><span data-stu-id="11276-107">Doing so can cause the application to block indefinitely, for the following reason:</span></span>

<span data-ttu-id="11276-108">Impossibile chiudere i thread all'interno di una funzione del punto di ingresso della DLL.</span><span class="sxs-lookup"><span data-stu-id="11276-108">Threads cannot exit while inside a DLL's entry-point function.</span></span> <span data-ttu-id="11276-109">Il kernel 32 include un blocco globale del processo durante la funzione del punto di ingresso e il blocco impedisce la chiusura del thread.</span><span class="sxs-lookup"><span data-stu-id="11276-109">Kernel 32 holds a global process lock during the entry-point function, and the lock prevents the thread from exiting.</span></span> <span data-ttu-id="11276-110">Poiché alcuni oggetti DirectShow sono proprietari di thread, possono bloccarsi se rilasciati dall'interno di una funzione del punto di ingresso della DLL.</span><span class="sxs-lookup"><span data-stu-id="11276-110">Because some DirectShow objects own threads, they can block if released from inside a DLL entry-point function.</span></span> <span data-ttu-id="11276-111">Se un'applicazione dispone di un oggetto C++ globale, la DLL di runtime C chiama il distruttore dell'oggetto quando la DLL viene scaricata.</span><span class="sxs-lookup"><span data-stu-id="11276-111">If an application has a global C++ object, the C runtime DLL calls the object's destructor when the DLL is unloaded.</span></span> <span data-ttu-id="11276-112">Se il distruttore rilascia oggetti DirectShow, può bloccarsi di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="11276-112">If the destructor releases DirectShow objects, it can block as a result.</span></span>

<span data-ttu-id="11276-113">Per motivi simili, una DLL non deve creare o rilasciare oggetti DirectShow nella relativa routine del punto di ingresso.</span><span class="sxs-lookup"><span data-stu-id="11276-113">For similar reasons, a DLL should not create or release DirectShow objects in its entry point routine.</span></span>

<span data-ttu-id="11276-114">**Rilascio di interfacce**</span><span class="sxs-lookup"><span data-stu-id="11276-114">**Releasing Interfaces**</span></span>

<span data-ttu-id="11276-115">È consigliabile rilasciare tutti i puntatori dell'interfaccia DirectShow mentre l'applicazione sta ancora elaborando i messaggi, prima di uscire dal ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="11276-115">You should release all DirectShow interface pointers while your application is still processing messages, before it exits the message loop.</span></span> <span data-ttu-id="11276-116">In caso contrario, è possibile che vengano visualizzate varie asserzioni perché alcuni oggetti DirectShow inviano messaggi durante le routine di pulizia.</span><span class="sxs-lookup"><span data-stu-id="11276-116">Otherwise, you might see various asserts, because some DirectShow objects send messages during their clean-up routines.</span></span>

<span data-ttu-id="11276-117">(Come corollario, se si utilizza la classe ATL **CWindowImpl** , non attendere che **OnFinalMessage** non liberi le interfacce.</span><span class="sxs-lookup"><span data-stu-id="11276-117">(As a corollary, if you are using the ATL **CWindowImpl** class, do not wait until **OnFinalMessage** to free the interfaces.</span></span> <span data-ttu-id="11276-118">Liberarli invece quando si gestisce il messaggio di \_ chiusura WM.</span><span class="sxs-lookup"><span data-stu-id="11276-118">Instead, free them when you handle the WM\_CLOSE message.)</span></span>

<span data-ttu-id="11276-119">**Conteggi dei riferimenti**</span><span class="sxs-lookup"><span data-stu-id="11276-119">**Reference Counts**</span></span>

<span data-ttu-id="11276-120">Quando la versione di debug di Quartz.dll viene scaricata, verifica se gli oggetti DirectShow hanno conteggi dei riferimenti che non sono stati rilasciati.</span><span class="sxs-lookup"><span data-stu-id="11276-120">When the debug version of Quartz.dll unloads, it checks whether any DirectShow objects have reference counts that were not released.</span></span> <span data-ttu-id="11276-121">In tal caso, viene generata un'asserzione:</span><span class="sxs-lookup"><span data-stu-id="11276-121">If so, it throws an assertion:</span></span>


```C++
g_cFGObjects == 0 
```



<span data-ttu-id="11276-122">Quando l'asserzione ha esito negativo, significa che l'applicazione ha perso un conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="11276-122">When this assertion fails, it means your application has leaked a reference count.</span></span> <span data-ttu-id="11276-123">Esaminare il codice e assicurarsi di rilasciare tutti i puntatori di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="11276-123">Review your code and make sure that you release all interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11276-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11276-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11276-125">Debug in DirectShow</span><span class="sxs-lookup"><span data-stu-id="11276-125">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



