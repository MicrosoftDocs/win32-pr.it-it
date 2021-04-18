---
title: Marshalling dell'interfaccia
description: Marshalling dell'interfaccia
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300498"
---
# <a name="interface-marshaling"></a><span data-ttu-id="3b436-103">Marshalling dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="3b436-103">Interface Marshaling</span></span>

<span data-ttu-id="3b436-104">A meno che non si conoscano tutti i dubbi che l'interfaccia non verrà mai usata tra i limiti di Apartment, thread o processo, è necessario decidere come fornire supporto per il marshalling per le interfacce.</span><span class="sxs-lookup"><span data-stu-id="3b436-104">Unless you know beyond all doubt that your interface will never be used across apartment, thread, or process boundaries, you need to decide how to provide marshaling support for your interfaces.</span></span> <span data-ttu-id="3b436-105">Sono disponibili tre modi per fornire supporto per il marshalling:</span><span class="sxs-lookup"><span data-stu-id="3b436-105">There are three ways to provide marshaling support:</span></span>

-   <span data-ttu-id="3b436-106">Scrivere il proprio codice proxy/stub che chiama il canale COM, che a sua volta chiama le librerie di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="3b436-106">Write your own proxy/stub code that calls the COM channel, which in turn calls the RPC run-time libraries.</span></span> <span data-ttu-id="3b436-107">In teoria, è possibile eseguire questa operazione, ma in pratica è quasi impossibile eseguire senza una notevole quantità di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3b436-107">Theoretically, it is possible to do this, but in practice it is almost impossible to do without a significant amount of effort.</span></span>
-   <span data-ttu-id="3b436-108">Descrivere le interfacce in un file IDL (Interface Definition Language) e usare il compilatore MIDL per generare una DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="3b436-108">Describe your interfaces in an interface definition language (IDL) file and use the MIDL compiler to generate a proxy/stub DLL.</span></span> <span data-ttu-id="3b436-109">Questo metodo offre le migliori prestazioni e la massima flessibilità in termini di tipi di dati accettabili.</span><span class="sxs-lookup"><span data-stu-id="3b436-109">This method provides the best performance and the most flexibility in terms of acceptable data types.</span></span> <span data-ttu-id="3b436-110">Usando stub proxy generati da MIDL, è possibile controllare non solo la gestione della memoria, ma anche il marshalling e l'unmarshalling di tipi di dati complessi su piattaforme diverse.</span><span class="sxs-lookup"><span data-stu-id="3b436-110">Using MIDL-generated proxy stubs, you can control not only memory management but even the marshaling and unmarshaling of complex data types across different platforms.</span></span>
-   <span data-ttu-id="3b436-111">Utilizzare MIDL per generare una libreria dei tipi utilizzata dal sistema per fornire supporto per il marshalling in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3b436-111">Use MIDL to generate a type library that the system uses to provide marshaling support at run time.</span></span> <span data-ttu-id="3b436-112">Questo è il modo più semplice per implementare il supporto del marshalling.</span><span class="sxs-lookup"><span data-stu-id="3b436-112">This is the easiest way to implement marshaling support.</span></span> <span data-ttu-id="3b436-113">È sufficiente generare una libreria di tipi e registrarla.</span><span class="sxs-lookup"><span data-stu-id="3b436-113">All you have to do is generate a type library and register it.</span></span> <span data-ttu-id="3b436-114">Le interfacce devono essere compatibili con l'automazione ( [**oleautomation**](/windows/desktop/Midl/oleautomation) o [**Dual**](/windows/desktop/Midl/dual)), che pone alcune restrizioni sui tipi di dati che è possibile usare come parametri del metodo.</span><span class="sxs-lookup"><span data-stu-id="3b436-114">Your interfaces must be Automation-compatible (either [**oleautomation**](/windows/desktop/Midl/oleautomation) or [**dual**](/windows/desktop/Midl/dual)), which places some restrictions on the kinds of data types you can use as method parameters.</span></span> <span data-ttu-id="3b436-115">Tuttavia, nella maggior parte dei casi, il vantaggio di avere le interfacce accessibili ai programmi scritti in altri linguaggi, ad esempio Microsoft Visual Basic e Java, supera le limitazioni dei tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="3b436-115">However, in most cases, the advantage of having your interfaces accessible to programs written in other languages, such as Microsoft Visual Basic and Java, outweighs the limitations on data types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b436-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b436-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b436-117">Comunicazione tra oggetti</span><span class="sxs-lookup"><span data-stu-id="3b436-117">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> </dl>

 

 