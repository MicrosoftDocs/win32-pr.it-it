---
title: Concetti relativi alla programmazione C++ e OLE
description: Concetti relativi alla programmazione C++ e OLE
ms.assetid: 2c6c3f29-aa5d-4e55-8c4d-16c5fb223fb9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c47ef5ff2d89930b5d4138f12e3ebc15385a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856945"
---
# <a name="c-and-ole-programming-concepts"></a><span data-ttu-id="edfdc-103">Concetti relativi alla programmazione C++ e OLE</span><span class="sxs-lookup"><span data-stu-id="edfdc-103">C++ and OLE Programming Concepts</span></span>

<span data-ttu-id="edfdc-104">I gestori di file e flussi inclusi in Windows utilizzano una progettazione orientata a oggetti per promuovere un'interfaccia standard e condividere le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="edfdc-104">The file and stream handlers included with Windows use an object-oriented design to promote a standard interface and to share functionality.</span></span> <span data-ttu-id="edfdc-105">Questi gestori sono scritti in C++ e usano il Component Object Model OLE.</span><span class="sxs-lookup"><span data-stu-id="edfdc-105">These handlers are written in C++ and use the OLE Component Object Model.</span></span>

<span data-ttu-id="edfdc-106">È possibile sviluppare gestori personalizzati usando i sistemi di sviluppo C o C++. Tuttavia, l'uso di C++ è fortemente consigliato, perché fornisce un approccio più semplice e più semplice per implementare un gestore.</span><span class="sxs-lookup"><span data-stu-id="edfdc-106">You can develop custom handlers using the C or C++ development systems; however, using C++ is strongly recommended, because it provides an easier and more straightforward approach to implement a handler.</span></span> <span data-ttu-id="edfdc-107">Con C++ è possibile definire in modo esplicito i dati come oggetti ed è possibile associare le funzioni che modificano i dati con le funzioni membro di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="edfdc-107">Using C++, you can explicitly define data as objects, and you can associate the functions that manipulate the data with the member functions of an object.</span></span>

<span data-ttu-id="edfdc-108">In questa sezione vengono identificati e brevemente riepilogati i concetti importanti di C++ e OLE Component Object Model che si applicano alla progettazione e all'implementazione di gestori di file e flussi.</span><span class="sxs-lookup"><span data-stu-id="edfdc-108">This section identifies and briefly summarizes the important concepts of C++ and the OLE Component Object Model that apply to designing and implementing file and stream handlers.</span></span> <span data-ttu-id="edfdc-109">Sono stati scritti molti libri sulla programmazione C++ a cui è possibile fare riferimento per ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="edfdc-109">There are many books written about C++ programming that you can reference for more information.</span></span> <span data-ttu-id="edfdc-110">Per ulteriori informazioni su OLE, vedere la Guida *di riferimento per programmatori OLE*.</span><span class="sxs-lookup"><span data-stu-id="edfdc-110">For more information on OLE, please see the *OLE Programmer's Reference*.</span></span>

 

 




