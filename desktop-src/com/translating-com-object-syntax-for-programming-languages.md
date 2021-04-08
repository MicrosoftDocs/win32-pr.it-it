---
title: Traduzione della sintassi degli oggetti COM per i linguaggi di programmazione
description: Traduzione della sintassi degli oggetti COM per i linguaggi di programmazione
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855998"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a><span data-ttu-id="818dd-103">Traduzione della sintassi degli oggetti COM per i linguaggi di programmazione</span><span class="sxs-lookup"><span data-stu-id="818dd-103">Translating COM Object Syntax for Programming Languages</span></span>

<span data-ttu-id="818dd-104">Per chiamare un oggetto COM da un'applicazione scritta in un linguaggio di programmazione diverso da quello usato per scrivere l'oggetto COM, è necessario innanzitutto tradurre la sintassi dell'oggetto nel linguaggio di programmazione.</span><span class="sxs-lookup"><span data-stu-id="818dd-104">To call a COM object from an application written in a programming language other than the one used to write the COM object, you must first translate the object's syntax to your programming language.</span></span> <span data-ttu-id="818dd-105">Per effettuare questa operazione, utilizzare la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="818dd-105">This can be done using the following steps:</span></span>

1.  <span data-ttu-id="818dd-106">Visualizzare la libreria dei tipi dell'oggetto COM nella sintassi del linguaggio di programmazione.</span><span class="sxs-lookup"><span data-stu-id="818dd-106">View the COM object's type library in your programming language's syntax.</span></span> <span data-ttu-id="818dd-107">In questo modo vengono fornite le descrizioni delle classi, delle interfacce, dei metodi, delle proprietà e degli eventi dell'oggetto nella sintassi del linguaggio in uso.</span><span class="sxs-lookup"><span data-stu-id="818dd-107">Doing this provides you with descriptions of the object's classes, interfaces, methods, properties and events in the language syntax you use.</span></span>

    <span data-ttu-id="818dd-108">I prodotti Microsoft Developer forniscono diversi strumenti per semplificare la visualizzazione e la conversione delle librerie dei tipi.</span><span class="sxs-lookup"><span data-stu-id="818dd-108">Microsoft developer products provide several tools to assist you in viewing and converting type libraries.</span></span> <span data-ttu-id="818dd-109">Per altre informazioni, vedere [visualizzatori e strumenti di conversione della libreria dei tipi](type-library-viewers-and-conversion-tools.md) e [come strumenti di sviluppo usare le librerie dei tipi](how-developer-tools-use-type-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="818dd-109">For more information, see [Type Library Viewers and Conversion Tools](type-library-viewers-and-conversion-tools.md) and [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

    <span data-ttu-id="818dd-110">Quando è possibile visualizzare la libreria dei tipi dell'oggetto nel linguaggio di programmazione preferito, è possibile confrontare la relativa sintassi con quella nella documentazione relativa all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="818dd-110">Once you can view the object's type library in your preferred programming language, you can compare its syntax to that in the documentation for the object.</span></span> <span data-ttu-id="818dd-111">Se l'oggetto è documentato in un linguaggio di programmazione diverso da quello in uso, i tipi di dati e la sintassi potrebbero essere diversi, ma le descrizioni dei parametri, i valori restituiti e la funzionalità dell'oggetto devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="818dd-111">If the object is documented in a programming language other than the one you are using, the data types and syntax may differ, but descriptions of parameters, return values, and the object's functionality should be the same.</span></span>

2.  <span data-ttu-id="818dd-112">Prendere in considerazione eventuali considerazioni speciali per la conversione nel linguaggio di programmazione.</span><span class="sxs-lookup"><span data-stu-id="818dd-112">Take into account any special considerations for translating to your programming language.</span></span>

    <span data-ttu-id="818dd-113">Poiché ogni linguaggio di programmazione definisce concetti che non possono avere un equivalente in altre lingue, alcune funzionalità di un oggetto possono funzionare in modo diverso in un altro linguaggio o non essere disponibili.</span><span class="sxs-lookup"><span data-stu-id="818dd-113">Because each programming language defines concepts that may not have an equivalent in other languages, some of an object's functionality may work differently in another language, or not be available at all.</span></span> <span data-ttu-id="818dd-114">Il linguaggio di programmazione Visual Basic, ad esempio, non riconosce i tipi di dati non firmati C++, ad esempio **unsignedÂ Long**.</span><span class="sxs-lookup"><span data-stu-id="818dd-114">For example, the Visual Basic programming language does not recognize C++ unsigned data types, such as **unsignedÂ long**.</span></span> <span data-ttu-id="818dd-115">Un'applicazione scritta in Visual Basic non può utilizzare metodi COM che accettano o restituiscono variabili con tipo di dati senza segno.</span><span class="sxs-lookup"><span data-stu-id="818dd-115">An application written in Visual Basic cannot use COM methods that accept or return unsigned data type variables.</span></span>

3.  <span data-ttu-id="818dd-116">Aggiungere il codice compilato dell'oggetto COM al progetto.</span><span class="sxs-lookup"><span data-stu-id="818dd-116">Add the COM object's compiled code to your project.</span></span> <span data-ttu-id="818dd-117">Il codice compilato è in genere contenuto in un file con estensione dll o ocx.</span><span class="sxs-lookup"><span data-stu-id="818dd-117">The compiled code is typically contained in a .dll or .ocx file.</span></span> <span data-ttu-id="818dd-118">Questo passaggio è necessario affinché il compilatore riconosca le classi dell'oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="818dd-118">This step is necessary for the compiler to recognize the COM object's classes.</span></span> <span data-ttu-id="818dd-119">Dopo aver aggiunto l'oggetto COM, l'applicazione può utilizzare le classi e le interfacce.</span><span class="sxs-lookup"><span data-stu-id="818dd-119">After you add the COM object, your application can use its classes and interfaces.</span></span>

<span data-ttu-id="818dd-120">Negli argomenti seguenti viene descritto come tradurre e utilizzare oggetti COM in un'ampia gamma di linguaggi di programmazione:</span><span class="sxs-lookup"><span data-stu-id="818dd-120">The following topics describe how to translate and use COM objects in a variety of programming languages:</span></span>

-   [<span data-ttu-id="818dd-121">Conversione in C++</span><span class="sxs-lookup"><span data-stu-id="818dd-121">Translating to C++</span></span>](translating-to-c--.md)
-   [<span data-ttu-id="818dd-122">Conversione in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="818dd-122">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
-   [<span data-ttu-id="818dd-123">Conversione in Java</span><span class="sxs-lookup"><span data-stu-id="818dd-123">Translating to Java</span></span>](translating-to-java.md)

<span data-ttu-id="818dd-124">Questi argomenti descrivono gli strumenti e i processi di conversione forniti dai prodotti Microsoft Developer.</span><span class="sxs-lookup"><span data-stu-id="818dd-124">These topics describe conversion tools and processes provided by Microsoft developer products.</span></span> <span data-ttu-id="818dd-125">Per istruzioni su come programmare gli oggetti COM usando gli strumenti di sviluppo creati da altre società, vedere la documentazione relativa agli strumenti di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="818dd-125">For instructions on how to program COM objects using development tools created by other companies, see those development tools' documentation.</span></span>

 

 




