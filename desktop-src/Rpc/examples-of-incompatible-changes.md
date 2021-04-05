---
title: Esempi di modifiche incompatibili
description: 'Quando si gestiscono modifiche incompatibili, la regola empirica sfavorevole è la seguente: qualsiasi modifica può essere incompatibile con le versioni precedenti, a meno che non sia ben riconosciuta.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044869"
---
# <a name="examples-of-incompatible-changes"></a><span data-ttu-id="0cf2a-103">Esempi di modifiche incompatibili</span><span class="sxs-lookup"><span data-stu-id="0cf2a-103">Examples of Incompatible Changes</span></span>

<span data-ttu-id="0cf2a-104">Quando si gestiscono modifiche incompatibili, la regola empirica sfavorevole è la seguente: qualsiasi modifica può essere incompatibile con le versioni precedenti, a meno che non sia ben riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-104">When dealing with incompatible changes, the unfortunate rule of thumb is as follows: any change can be backward incompatible, unless it is very well understood.</span></span> <span data-ttu-id="0cf2a-105">Questa regola richiede la conoscenza delle regole di mancato recapito.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-105">This rule requires knowledge of NDR rules.</span></span> <span data-ttu-id="0cf2a-106">Se non si conosce il rapporto di mancato recapito, non apportare modifiche.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-106">If you do not know what the NDR is, do not make modifications.</span></span> <span data-ttu-id="0cf2a-107">Di seguito sono riportati alcuni esempi di modifiche che in genere comportano una violazione di accesso nell'applicazione o un' \_ \_ eccezione dei dati stub non valida \_ generata dal motore di marshalling:</span><span class="sxs-lookup"><span data-stu-id="0cf2a-107">Examples of changes that typically result in an access violation in the application, or a BAD\_STUB\_DATA\_EXCEPTION raised by the marshaling engine, are as follows:</span></span>

-   <span data-ttu-id="0cf2a-108">Aggiunta di un nuovo metodo al centro dei metodi obsoleti.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-108">Adding a new method in the middle of old methods.</span></span>
-   <span data-ttu-id="0cf2a-109">Aggiunta o rimozione di parametri da un metodo.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-109">Adding or removing parameters from a method.</span></span>
-   <span data-ttu-id="0cf2a-110">Modifica di un attributo, ad esempio un attributo puntatore: \[ modifica \] di ref in \[ Unique \] o \[ ptr \] o viceversa.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-110">Changing an attribute, for example a pointer attribute: changing \[ref\] to \[unique\] or \[ptr\] or vice versa.</span></span> <span data-ttu-id="0cf2a-111">Ogni tipo di puntatore ha una rappresentazione Wire diversa.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-111">Each pointer type has a different wire representation.</span></span>
-   <span data-ttu-id="0cf2a-112">Modifica della dimensione dei dati: da short a Long, da char a WCHAR \_ t (Unicode), aggiungendo un campo a una struttura, modificando la dimensione di una matrice a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-112">Changing the size of the data: from short to long, from char to wchar\_t (unicode), adding a field to a structure, changing the size of a fixed size array.</span></span>
-   <span data-ttu-id="0cf2a-113">Aggiunta di Union Arms a un'Unione con una clausola default.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-113">Adding union arms to a union with a default clause.</span></span>

<span data-ttu-id="0cf2a-114">Alcune modifiche insidiose o mancate corrispondenze indesiderate tra un client e un server possono verificarsi come segue:</span><span class="sxs-lookup"><span data-stu-id="0cf2a-114">Some insidious changes or unintended mismatches between a client and a server may occur as follows:</span></span>

-   <span data-ttu-id="0cf2a-115">Modifica di un membro di un tipo composto, ad esempio una struttura o una matrice.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-115">Modifying a member of a compound type, like a structure or an array.</span></span> <span data-ttu-id="0cf2a-116">Se, ad esempio, un \_ ID client passa da un elemento integrale a un GUID, una \_ struttura di record client con il \_ campo ID client diventa incompatibile.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-116">For example, if a CLIENT\_ID changes from an integral to a GUID, a CLIENT\_RECORD structure with the CLIENT\_ID field becomes incompatible.</span></span> <span data-ttu-id="0cf2a-117">Questo può essere difficile da rilevare se viene propagata attraverso diversi livelli di incorporamento in un tipo di parametro remoto effettivo.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-117">This may be difficult to detect if cascaded through several levels of embedding to an actual remote parameter type.</span></span>
-   <span data-ttu-id="0cf2a-118">Modifica di un tipo importato.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-118">Modifying an imported type.</span></span> <span data-ttu-id="0cf2a-119">Il tipo può provenire da un componente diverso che non è direttamente remoto, di conseguenza la modifica è stata considerata compatibile.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-119">The type may be coming from a different component that does not remote directly, hence the change was thought to be compatible.</span></span>
-   <span data-ttu-id="0cf2a-120">L'uso di \# ifdef in un file IDL non è una buona idea per le definizioni di tipo di ifdef in un file IDL. si tratta di un'emergenza in attesa di verificarsi.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-120">Using \#ifdef in an IDL file is a bad idea to ifdef type definitions in an IDL file—it is disaster waiting to happen.</span></span> <span data-ttu-id="0cf2a-121">Inevitabilmente, a causa della compilazione o di altre anomalie, un client viene compilato con un set diverso di definizioni rispetto al server e non è più compatibile.</span><span class="sxs-lookup"><span data-stu-id="0cf2a-121">Inevitably, due to build or other glitches, a client is compiled with a different set of defines than the server, and they end up being incompatible.</span></span>

 

 




