---
title: File di configurazione dell'applicazione (ACF)
description: Potrebbero esserci aspetti dell'applicazione distribuita che interessano un componente, ma non hanno nulla a che fare con un altro componente.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- MIDL DI ACF
- Microsoft Interface Definition Language MIDL, descritto, file di configurazione dell'applicazione
- file di configurazione dell'applicazione MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298671"
---
# <a name="application-configuration-file-acf"></a><span data-ttu-id="a8c7d-106">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="a8c7d-106">Application Configuration File (ACF)</span></span>

<span data-ttu-id="a8c7d-107">Potrebbero esserci aspetti dell'applicazione distribuita che interessano un componente, ma non hanno nulla a che fare con un altro componente.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-107">There may be aspects of your distributed application that affect one component, but have nothing to do with another.</span></span> <span data-ttu-id="a8c7d-108">Ad esempio, un oggetto può contenere una struttura di dati complessa e di grandi dimensioni e passare il contenuto di questa struttura di dati a un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-108">For example, an object may contain a large, complex data structure and pass the contents of this data structure to another object.</span></span> <span data-ttu-id="a8c7d-109">Il layout esatto di questa struttura di dati potrebbe non essere significativo per l'applicazione ricevente.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-109">The exact layout of this data structure may be meaningless to the receiving application.</span></span> <span data-ttu-id="a8c7d-110">Inoltre, la struttura può contenere tipi di dati che il compilatore MIDL non riconosce e non può generare codice di marshalling e di unmarshalling.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-110">Also, the structure may contain data types that the MIDL compiler does not recognize and cannot generate marshaling and unmarshaling code.</span></span>

<span data-ttu-id="a8c7d-111">Le applicazioni client possono condividere la stessa interfaccia ma possono essere eseguite su piattaforme diverse; ognuno può avere bisogno di un proprio set di routine di marshalling.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-111">Client applications may share the same interface but run on different platforms; they may each need their own set of marshaling routines.</span></span> <span data-ttu-id="a8c7d-112">Infine, i singoli client potrebbero non avere sempre lo stesso set di funzioni.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-112">Finally, individual clients may not always need the same set of functions.</span></span> <span data-ttu-id="a8c7d-113">Non è efficiente generare codice stub per le funzioni che non verranno mai implementate in un'applicazione client specifica.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-113">It is inefficient to generate stub code for functions that will never be implemented in a particular client application.</span></span>

<span data-ttu-id="a8c7d-114">Definendo questi aspetti locali dell'interfaccia in un file di configurazione dell'applicazione (ACF), è possibile separare le differenze tra le interfacce client dalla relativa rappresentazione di rete, consentendo al server di inviare e ricevere dati in un formato coerente, rendendo il codice stub più compatto ed efficiente.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-114">By defining these local aspects of your interface in an application configuration file (ACF), you can separate the differences between the client interfaces from their network representation, allowing the server to send and receive data in a consistent format, and making your stub code more compact and efficient.</span></span>

<span data-ttu-id="a8c7d-115">La struttura e la sintassi di una definizione di interfaccia ACF sono identiche alla definizione IDL:</span><span class="sxs-lookup"><span data-stu-id="a8c7d-115">The structure and syntax of an ACF interface definition are identical to the IDL definition:</span></span>

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

<span data-ttu-id="a8c7d-116">Per impostazione predefinita, il nome dell'interfaccia ACF deve corrispondere al nome nella definizione IDL.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-116">By default, the ACF interface name must match its name in the IDL definition.</span></span> <span data-ttu-id="a8c7d-117">Tuttavia, quando si usa l'opzione del compilatore MIDL/ [**ACF**](-acf.md) per specificare in modo esplicito un nome di file ACF, non è necessario che i nomi di interfaccia corrispondano.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-117">However, when you use the MIDL compiler option / [**acf**](-acf.md) to explicitly specify an ACF file name, the interface names do not have to match.</span></span> <span data-ttu-id="a8c7d-118">Questa funzionalità consente a diverse interfacce di condividere una singola specifica ACF.</span><span class="sxs-lookup"><span data-stu-id="a8c7d-118">This feature allows several interfaces to share a single ACF specification.</span></span>

 

 




