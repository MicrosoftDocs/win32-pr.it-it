---
title: Progettazione di interfacce compatibili con 64 bit
description: I problemi di compatibilità con le versioni precedenti si verificano quando si aggiungono nuovi tipi di dati o metodi a un'interfaccia, si modificano i tipi di dati obsoleti o si utilizzano i tipi di dati
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- Programmazione Windows con compatibilità con le versioni precedenti a 64 bit
- interfacce a 64 bit compatibili con la programmazione Windows a 64 bit
- Guida alla programmazione di Windows a 64 bit, programmazione Windows a 64 bit, compatibilità
- compatibilità con la programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329812"
---
# <a name="designing-64-bit-compatible-interfaces"></a><span data-ttu-id="77807-107">Progettazione di interfacce compatibili con 64 bit</span><span class="sxs-lookup"><span data-stu-id="77807-107">Designing 64-bit-Compatible Interfaces</span></span>

<span data-ttu-id="77807-108">Il porting da Windows a 32 bit a Windows a 64 bit non dovrebbe, da solo, creare eventuali problemi per le applicazioni distribuite, indipendentemente dal fatto che usino chiamate a procedure remote (RPC) direttamente o tramite DCOM.</span><span class="sxs-lookup"><span data-stu-id="77807-108">Porting from 32-bit Windows to 64-bit Windows should not, by itself, create any problems for distributed applications, whether they use Remote Procedure Calls (RPC) directly or through DCOM.</span></span> <span data-ttu-id="77807-109">Il modello di programmazione RPC specifica le dimensioni dei dati ben definite e i tipi integer con le stesse dimensioni a ogni estremità della connessione.</span><span class="sxs-lookup"><span data-stu-id="77807-109">The RPC programming model specifies well-defined data sizes and integer types that are the same size on each end of the connection.</span></span> <span data-ttu-id="77807-110">Inoltre, nel modello di dati LLP64 abstract sviluppato per Windows a 64 bit, solo i puntatori si espandono a 64 bit. tutti gli altri tipi di dati Integer rimangono 32 bit.</span><span class="sxs-lookup"><span data-stu-id="77807-110">Also, in the LLP64 abstract data model developed for 64-bit Windows, only the pointers expand to 64 bits—all other integer data types remain 32 bits.</span></span> <span data-ttu-id="77807-111">Poiché i puntatori sono locali a ogni lato della connessione client/server e vengono in genere trasmessi come marcatori **null** o non **null** , il motore di marshalling è in grado di gestire in modo trasparente diverse dimensioni del puntatore a una delle estremità di una connessione.</span><span class="sxs-lookup"><span data-stu-id="77807-111">Because pointers are local to each side of the client/server connection and are usually transmitted as **NULL** or non-**NULL** markers, the marshaling engine can handle different pointer sizes on either end of a connection transparently.</span></span>

<span data-ttu-id="77807-112">Tuttavia, si verificano problemi di compatibilità con le versioni precedenti quando si aggiungono nuovi tipi di dati o metodi a un'interfaccia, si modificano i tipi di dati obsoleti o si utilizzano i tipi di dati in modo</span><span class="sxs-lookup"><span data-stu-id="77807-112">However, backward compatibility issues arise when you add new data types or methods to an interface, change old data types, or use data types inappropriately.</span></span> <span data-ttu-id="77807-113">Negli argomenti seguenti viene illustrato come evitare queste situazioni, se possibile, e come progettare soluzioni alternative affidabili quando non è possibile evitarle.</span><span class="sxs-lookup"><span data-stu-id="77807-113">The following topics discuss how to avoid these situations (when possible) and how to design robust workarounds when it is not possible to avoid them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77807-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="77807-114">In this Section</span></span>

-   [<span data-ttu-id="77807-115">Modifica di un'interfaccia esistente</span><span class="sxs-lookup"><span data-stu-id="77807-115">Changing an Existing Interface</span></span>](changing-an-existing-interface.md)
-   [<span data-ttu-id="77807-116">Evitare le informazioni nascoste</span><span class="sxs-lookup"><span data-stu-id="77807-116">Avoiding Information Hiding</span></span>](avoiding-information-hiding.md)
-   [<span data-ttu-id="77807-117">Evitare il polimorfismo</span><span class="sxs-lookup"><span data-stu-id="77807-117">Avoiding Polymorphism</span></span>](avoiding-polymorphism.md)
-   [<span data-ttu-id="77807-118">Uso di nuovi tipi di dati nel file IDL</span><span class="sxs-lookup"><span data-stu-id="77807-118">Using New Data Types in Your IDL File</span></span>](using-new-data-types-in-your-idl-file.md)
-   [<span data-ttu-id="77807-119">Preparazione dell'applicazione per Windows a 64 bit</span><span class="sxs-lookup"><span data-stu-id="77807-119">Preparing Your Application for 64-bit Windows</span></span>](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a><span data-ttu-id="77807-120">Sezioni correlate</span><span class="sxs-lookup"><span data-stu-id="77807-120">Related Sections</span></span>

<span data-ttu-id="77807-121">Se non si ha già familiarità con i nuovi tipi di dati, l'ambiente di lavoro e le modifiche dell'API per Windows a 64 bit, vedere [preparazione per Windows a 64 bit](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="77807-121">If you are not already familiar with the new data types, working environment, and API changes for 64-bit Windows, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

 

 




