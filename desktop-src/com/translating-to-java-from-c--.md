---
title: Conversione in Java da C++
description: Utilizzando il linguaggio di programmazione C++, gli sviluppatori possono accedere direttamente alla memoria che archivia una determinata variabile. I puntatori alla memoria forniscono questo accesso diretto. In Java, i puntatori vengono gestiti per l'utente.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395410"
---
# <a name="translating-to-java-from-c"></a><span data-ttu-id="0aa9f-105">Conversione in Java da C++</span><span class="sxs-lookup"><span data-stu-id="0aa9f-105">Translating to Java from C++</span></span>

<span data-ttu-id="0aa9f-106">Utilizzando il linguaggio di programmazione C++, gli sviluppatori possono accedere direttamente alla memoria che archivia una determinata variabile.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-106">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="0aa9f-107">I puntatori alla memoria forniscono questo accesso diretto.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-107">Memory pointers provide this direct access.</span></span> <span data-ttu-id="0aa9f-108">In Java, i puntatori vengono gestiti per l'utente.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-108">In Java, pointers are handled for you.</span></span>

<span data-ttu-id="0aa9f-109">Nei tipi di dati compositi Java, **struct**, **Union** e **typedef** vengono gestiti esclusivamente tramite l'utilizzo delle classi.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-109">In Java, **struct**, **union**, and **typedef** composite data types are handled exclusively through the use of classes.</span></span> <span data-ttu-id="0aa9f-110">Il tipo di dati **Variant** C++, ad esempio, esegue il mapping a **com. ms. com. Variant** in Java.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-110">For example, the C++ **VARIANT** data type maps to **com.ms.com.Variant** in Java.</span></span>

<span data-ttu-id="0aa9f-111">In C++, le stringhe sono una matrice di caratteri.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-111">In C++, strings are an array of characters.</span></span> <span data-ttu-id="0aa9f-112">In Java le stringhe sono oggetti.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-112">In Java, strings are objects.</span></span> <span data-ttu-id="0aa9f-113">I metodi che agiscono sulle stringhe gestiscono la stringa come oggetto completo.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-113">Methods that act on strings treat the string as a complete object.</span></span>

<span data-ttu-id="0aa9f-114">I metodi COM restituiscono un valore noto come **HRESULT**, ovvero un codice di errore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-114">COM methods return a value known as a **HRESULT**, which is a 32-bit error code.</span></span> <span data-ttu-id="0aa9f-115">Il supporto Java per Microsoft Internet Explorer definisce una classe, **com. ms. com. COMException**, che esegue il wrapping del codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0aa9f-115">The Java support for Microsoft Internet Explorer defines a class, **com.ms.com.ComException**, which wraps the **HRESULT** error code.</span></span>

<span data-ttu-id="0aa9f-116">Java non supporta i tipi di dati senza segno ad eccezione di **char**, che è un Unsigned Integer a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-116">Java does not support unsigned data types except for **char**, which is a 16-bit unsigned integer.</span></span> <span data-ttu-id="0aa9f-117">I metodi che accettano o restituiscono altri tipi di dati non firmati non possono essere usati da Java.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-117">Methods that accept or return other unsigned data types cannot be used from Java.</span></span>

<span data-ttu-id="0aa9f-118">Java non supporta le matrici multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-118">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="0aa9f-119">I metodi che accettano o restituiscono matrici multidimensionali non sono disponibili in Java.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-119">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="0aa9f-120">Non è possibile eseguire il cast dei valori booleani in Java a 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="0aa9f-120">Boolean values in Java cannot be cast to 0 and 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aa9f-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0aa9f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aa9f-122">Conversione in Java</span><span class="sxs-lookup"><span data-stu-id="0aa9f-122">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




