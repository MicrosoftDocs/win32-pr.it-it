---
description: Un parser è il componente Network Monitor che controlla i dati in un'acquisizione ritardata e passa informazioni specifiche sul protocollo all'applicazione che chiama il parser. Un parser è passivo perché funziona solo quando Network Monitor o un esperto lo chiama.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878634"
---
# <a name="parser"></a><span data-ttu-id="4b56c-104">Parser</span><span class="sxs-lookup"><span data-stu-id="4b56c-104">Parser</span></span>

<span data-ttu-id="4b56c-105">Un parser è il componente Network Monitor che controlla i dati in un' [*acquisizione ritardata*](d.md)e passa informazioni specifiche sul protocollo all'applicazione che chiama il parser.</span><span class="sxs-lookup"><span data-stu-id="4b56c-105">A parser is the Network Monitor component that inspects data in a [*delayed capture*](d.md), and passes specific protocol information to the application that calls the parser.</span></span> <span data-ttu-id="4b56c-106">Un parser è passivo perché funziona solo quando Network Monitor o un [*esperto*](e.md) lo chiama.</span><span class="sxs-lookup"><span data-stu-id="4b56c-106">A parser is passive because it works only when Network Monitor or an [*expert*](e.md) call it.</span></span>

<span data-ttu-id="4b56c-107">Ogni parser identifica un protocollo e in genere un parser viene implementato all'interno della propria DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="4b56c-107">Each parser identifies one protocol, and typically, a parser is implemented within its own parser DLL.</span></span> <span data-ttu-id="4b56c-108">Una DLL del parser può tuttavia contenere più parser, il che significa che una DLL può essere usata per rilevare più di un protocollo.</span><span class="sxs-lookup"><span data-stu-id="4b56c-108">However, a parser DLL can contain multiple parsers which means that one DLL can be used to detect more than one protocol.</span></span>

<span data-ttu-id="4b56c-109">I dati passati a un parser vengono ricavati da un' [*acquisizione ritardata*](d.md)e passati al parser in base ai frame.</span><span class="sxs-lookup"><span data-stu-id="4b56c-109">The data passed to a parser is taken from a [*delayed capture*](d.md), and passed to the parser on a frame-by-frame basis.</span></span> <span data-ttu-id="4b56c-110">Non è possibile analizzare un'acquisizione in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="4b56c-110">You cannot parse a real-time capture.</span></span>

<span data-ttu-id="4b56c-111">Per analizzare i dati in un frame, il parser deve riconoscere l'istanza del protocollo, identificare le proprietà presenti nell'istanza del protocollo e alleghi una definizione di proprietà a ogni proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b56c-111">To parse the data in a frame, the parser must recognize the protocol instance, identify the properties that exist in the protocol instance, and attach a property definition to each property.</span></span> <span data-ttu-id="4b56c-112">Tenere presente che il frame contiene solo un flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="4b56c-112">Be aware that the frame contains only a stream of data.</span></span> <span data-ttu-id="4b56c-113">Il frame non contiene dati che indicano quali protocolli o proprietà del protocollo rappresentano i dati.</span><span class="sxs-lookup"><span data-stu-id="4b56c-113">The frame does not contain data that indicates which protocols or protocol properties the data represents.</span></span>

<span data-ttu-id="4b56c-114">Nella figura seguente viene illustrato un frame contenente un'istanza di un protocollo.</span><span class="sxs-lookup"><span data-stu-id="4b56c-114">The following illustration shows a frame that contains an instance of a protocol.</span></span>

![frame che contiene un'istanza di protocollo](images/parser1.png)

<span data-ttu-id="4b56c-116">Se Network Monitor Visualizza i dati analizzati nell'interfaccia utente, il parser deve formattare i dati.</span><span class="sxs-lookup"><span data-stu-id="4b56c-116">If Network Monitor is going to display parsed data in the UI, the parser must format the data.</span></span> <span data-ttu-id="4b56c-117">Tuttavia, alcuni esperti usano l'output del parser a livello di codice e non visualizzano l'output nell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="4b56c-117">However, some experts use the parser output programmatically, and do not display the output in the Network Monitor UI.</span></span> <span data-ttu-id="4b56c-118">I dati visualizzati includono i dati definiti dal parser e i dati nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4b56c-118">Displayed data includes both parser-defined data, and the data in the capture.</span></span> <span data-ttu-id="4b56c-119">Il parser, ad esempio, in genere fornisce un nome per una proprietà visualizzata e i dati nell'acquisizione associata alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b56c-119">For example, the parser typically provides both a name for a property that is displayed, and the data in the capture that is associated with the property.</span></span>



| <span data-ttu-id="4b56c-120">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="4b56c-120">For information about</span></span>                                         | <span data-ttu-id="4b56c-121">Vedere</span><span class="sxs-lookup"><span data-stu-id="4b56c-121">See</span></span>                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="4b56c-122">Quali punti di ingresso devono essere implementati all'interno della DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="4b56c-122">Which entry points must be implemented within the parser DLL.</span></span> | [<span data-ttu-id="4b56c-123">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="4b56c-123">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                 |
| <span data-ttu-id="4b56c-124">Come implementare le funzioni di esportazione della DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="4b56c-124">How to implement parser DLL export functions.</span></span>                 | [<span data-ttu-id="4b56c-125">Scrittura di un parser di protocollo</span><span class="sxs-lookup"><span data-stu-id="4b56c-125">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="4b56c-126">Funzioni e parser di strutture utilizzati da.</span><span class="sxs-lookup"><span data-stu-id="4b56c-126">Which functions and structures parsers use.</span></span>                   | [<span data-ttu-id="4b56c-127">Funzioni e strutture del parser</span><span class="sxs-lookup"><span data-stu-id="4b56c-127">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



