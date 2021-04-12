---
title: Traduzioni in linguaggio COM
description: È possibile riutilizzare i componenti creati utilizzando il Component Object Model (COM) nelle applicazioni scritte in qualsiasi linguaggio di programmazione che supporti COM. Poiché COM è uno standard binario e, di conseguenza, è indipendente dal linguaggio.
ms.assetid: 89e74768-b7bd-4ab6-9129-9e677a9c14ca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f622b83b998402e82d6cf20975331645362c55e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395331"
---
# <a name="com-language-translations"></a><span data-ttu-id="0c65e-104">Traduzioni in linguaggio COM</span><span class="sxs-lookup"><span data-stu-id="0c65e-104">COM Language Translations</span></span>

<span data-ttu-id="0c65e-105">È possibile riutilizzare i componenti creati utilizzando il Component Object Model (COM) nelle applicazioni scritte in qualsiasi linguaggio di programmazione che supporti COM.</span><span class="sxs-lookup"><span data-stu-id="0c65e-105">Components created using the Component Object Model (COM) can be reused in applications written in any programming language that supports COM.</span></span> <span data-ttu-id="0c65e-106">Poiché COM è uno standard binario e, di conseguenza, è indipendente dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="0c65e-106">This is because COM is a binary standard and, as such, is language-independent.</span></span>

<span data-ttu-id="0c65e-107">Gli oggetti COM sono documentati nel linguaggio di programmazione o nelle lingue più rilevanti.</span><span class="sxs-lookup"><span data-stu-id="0c65e-107">COM objects are documented in the most relevant programming language or languages.</span></span> <span data-ttu-id="0c65e-108">Ad esempio, gli oggetti creati per l'utilizzo nelle pagine Web sono in genere documentati nel sistema di sviluppo Visual Basic Microsoft, mentre gli oggetti a livello di sistema sono in genere documentati in C++.</span><span class="sxs-lookup"><span data-stu-id="0c65e-108">For example, objects that are created for use in webpages are typically documented in the Microsoft Visual Basic development system, whereas system-level objects are typically documented in C++.</span></span> <span data-ttu-id="0c65e-109">Tuttavia, poiché COM è indipendente dalla lingua, non si è limitati all'utilizzo di un oggetto nella stessa lingua in cui è scritto o documentato.</span><span class="sxs-lookup"><span data-stu-id="0c65e-109">However, because COM is language-neutral, you are not limited to using an object in the same language in which it is written or documented.</span></span> <span data-ttu-id="0c65e-110">Ad esempio, è possibile scrivere un'applicazione in JScript che usa un controllo creato in C++ e documentato in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0c65e-110">For example, you can write an application in JScript that uses a control created in C++ and documented in Visual Basic.</span></span>

<span data-ttu-id="0c65e-111">Negli argomenti seguenti vengono illustrate le differenze tra i linguaggi di programmazione e viene descritto come tradurre la sintassi degli oggetti COM da un linguaggio a un altro.</span><span class="sxs-lookup"><span data-stu-id="0c65e-111">The following topics discuss the differences between programming languages and describe how to translate COM object syntax from one language to another.</span></span> <span data-ttu-id="0c65e-112">Altri argomenti descrivono come usare gli oggetti COM in diversi linguaggi e ambienti di scripting.</span><span class="sxs-lookup"><span data-stu-id="0c65e-112">Additional topics describe how to use COM objects in various scripting languages and environments.</span></span>

-   [<span data-ttu-id="0c65e-113">Differenze di sintassi</span><span class="sxs-lookup"><span data-stu-id="0c65e-113">Syntax Differences</span></span>](syntax-differences.md)
-   [<span data-ttu-id="0c65e-114">Conversioni di tipi di dati</span><span class="sxs-lookup"><span data-stu-id="0c65e-114">Data Type Conversions</span></span>](data-type-conversions.md)
-   [<span data-ttu-id="0c65e-115">File IDL</span><span class="sxs-lookup"><span data-stu-id="0c65e-115">IDL Files</span></span>](idl-files.md)
-   [<span data-ttu-id="0c65e-116">Traduzione della sintassi degli oggetti COM per i linguaggi di programmazione</span><span class="sxs-lookup"><span data-stu-id="0c65e-116">Translating COM Object Syntax for Programming Languages</span></span>](translating-com-object-syntax-for-programming-languages.md)
-   [<span data-ttu-id="0c65e-117">Creazione di script con oggetti COM</span><span class="sxs-lookup"><span data-stu-id="0c65e-117">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)

<span data-ttu-id="0c65e-118">Lo scopo è quello di risolvere i problemi più comuni di traduzione della lingua che si verificano quando si usano oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="0c65e-118">The intent is to address the most common language translation issues that arise when using COM objects.</span></span> <span data-ttu-id="0c65e-119">Le tecniche e i principi descritti si applicano a qualsiasi linguaggio di programmazione o script che supporta COM.</span><span class="sxs-lookup"><span data-stu-id="0c65e-119">The techniques and principles described apply to any programming or scripting language that supports COM.</span></span> <span data-ttu-id="0c65e-120">Poiché i linguaggi di scripting e i linguaggi di programmazione rappresentano paradigmi di programmazione diversi, la conversione tra linguaggi di scripting e linguaggi di programmazione non viene risolta.</span><span class="sxs-lookup"><span data-stu-id="0c65e-120">Because scripting languages and programming languages represent different programming paradigms, translation between scripting languages and programming languages is not addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c65e-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c65e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c65e-122">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="0c65e-122">Component Object Model (COM)</span></span>](component-object-model--com--portal.md)
</dt> </dl>

 

 




