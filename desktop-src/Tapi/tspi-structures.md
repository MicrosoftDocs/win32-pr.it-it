---
description: Le strutture di dati utilizzate da TSPI sono identiche a quelle definite nelle strutture TAPI, ad eccezione di TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Strutture TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311850"
---
# <a name="tspi-structures"></a><span data-ttu-id="b4823-103">Strutture TSPI</span><span class="sxs-lookup"><span data-stu-id="b4823-103">TSPI Structures</span></span>

<span data-ttu-id="b4823-104">Le strutture di dati utilizzate da TSPI sono identiche a quelle definite nelle [strutture TAPI](./tapi-structures.md), ad eccezione di [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span><span class="sxs-lookup"><span data-stu-id="b4823-104">The data structures TSPI uses are identical to those defined in [TAPI Structures](./tapi-structures.md), with the exception of [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span></span>

<span data-ttu-id="b4823-105">Nel caso della maggior parte delle strutture di dati più grandi, la responsabilità di compilare i membri è divisa tra il provider di servizi e TAPI.</span><span class="sxs-lookup"><span data-stu-id="b4823-105">In the case of most of the larger data structures, the responsibility for filling in members is divided between the service provider and TAPI.</span></span> <span data-ttu-id="b4823-106">Il provider di servizi deve mantenere i valori presenti nei membri di proprietà di TAPI.</span><span class="sxs-lookup"><span data-stu-id="b4823-106">The service provider must preserve the values present in members owned by TAPI.</span></span> <span data-ttu-id="b4823-107">La descrizione dei membri che devono essere impostati dal provider di servizi e che devono essere conservati viene fornita nella sezione funzioni delle funzioni che fanno riferimento a tale struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="b4823-107">The description of which members must be set by the service provider and which must be preserved is provided in the Functions section in the functions that refer to that data structure.</span></span>

<span data-ttu-id="b4823-108">Per ogni struttura, nella sezione Reference sono elencati gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4823-108">For each structure, the reference section lists the following items:</span></span>

-   <span data-ttu-id="b4823-109">Scopo della struttura</span><span class="sxs-lookup"><span data-stu-id="b4823-109">The purpose of the structure</span></span>
-   <span data-ttu-id="b4823-110">Descrizione dei valori o dei campi</span><span class="sxs-lookup"><span data-stu-id="b4823-110">A description of the values or fields</span></span>
-   <span data-ttu-id="b4823-111">Descrizione dell'estendibilità della struttura</span><span class="sxs-lookup"><span data-stu-id="b4823-111">A description of the structure's extensibility</span></span>
-   <span data-ttu-id="b4823-112">Commenti facoltativi sull'utilizzo della struttura</span><span class="sxs-lookup"><span data-stu-id="b4823-112">Optional comments about using the structure</span></span>
-   <span data-ttu-id="b4823-113">Riferimenti facoltativi ad altre funzioni, messaggi, costanti o strutture.</span><span class="sxs-lookup"><span data-stu-id="b4823-113">Optional references to other functions, messages, constants, or structures.</span></span>

<span data-ttu-id="b4823-114">Memoria per tutte le strutture di dati la cui rappresentazione è pubblicata e condivisa da TAPI e il provider di servizi viene allocato da TAPI o da un'applicazione che usa TAPI.</span><span class="sxs-lookup"><span data-stu-id="b4823-114">Memory for all data structures whose representation is published and shared by both TAPI and the service provider is allocated by TAPI or an application using TAPI.</span></span> <span data-ttu-id="b4823-115">TAPI passa un puntatore alla funzione TSPI che restituisce le informazioni.</span><span class="sxs-lookup"><span data-stu-id="b4823-115">TAPI passes a pointer to the TSPI function that returns the information.</span></span> <span data-ttu-id="b4823-116">TSPI riempie la struttura dei dati con le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="b4823-116">TSPI fills the data structure with the requested information.</span></span> <span data-ttu-id="b4823-117">Se l'operazione è asincrona, le informazioni non sono disponibili fino a quando il callback di risposta asincrona non indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b4823-117">If the operation is asynchronous, the information is not available until the asynchronous reply callback indicates success.</span></span>

> [!Note]  
> <span data-ttu-id="b4823-118">Alcune strutture includono campi di ridimensionamento e offset per la definizione della posizione e della lunghezza delle stringhe nella parte variabile della struttura.</span><span class="sxs-lookup"><span data-stu-id="b4823-118">Some structures include Size and Offset fields for defining the location and length of strings in the variable portion of the structure.</span></span> <span data-ttu-id="b4823-119">Se al provider di servizi viene richiesto di aggiungere una stringa ma non è disponibile alcuna stringa, il provider di servizi deve indicare questa condizione in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4823-119">If the service provider is requested to add a string but no string is available, the service provider must indicate this condition in one of these ways:</span></span>
>
> -   <span data-ttu-id="b4823-120">Impostare i campi dimensioni e offset su 0.</span><span class="sxs-lookup"><span data-stu-id="b4823-120">Set both the Size and Offset fields to 0.</span></span>
> -   <span data-ttu-id="b4823-121">Impostare il campo Offset su un valore diverso da zero, ma ridimensionarlo su 0.</span><span class="sxs-lookup"><span data-stu-id="b4823-121">Set the Offset field to nonzero but Size to 0.</span></span>
> -   <span data-ttu-id="b4823-122">Impostare il campo Offset su un valore diverso da zero, dimensioni su 1 e byte in corrispondenza dell'offset su 0.</span><span class="sxs-lookup"><span data-stu-id="b4823-122">Set the Offset field to nonzero, Size to 1, and the byte at the Offset to 0.</span></span>

 

 

 
