---
title: Conversione in C++ da Visual Basic
description: Visual Basic gestisce i puntatori in modo implicito. In C++, l'applicazione è responsabile dell'esecuzione di qualsiasi aritmetica del puntatore necessaria.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221388"
---
# <a name="translating-to-c-from-visual-basic"></a><span data-ttu-id="02ddf-104">Conversione in C++ da Visual Basic</span><span class="sxs-lookup"><span data-stu-id="02ddf-104">Translating to C++ from Visual Basic</span></span>

<span data-ttu-id="02ddf-105">Visual Basic gestisce i puntatori in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="02ddf-105">Visual Basic handles pointers implicitly.</span></span> <span data-ttu-id="02ddf-106">In C++, l'applicazione è responsabile dell'esecuzione di qualsiasi aritmetica del puntatore necessaria.</span><span class="sxs-lookup"><span data-stu-id="02ddf-106">In C++, your application is responsible for performing any necessary pointer arithmetic.</span></span>

<span data-ttu-id="02ddf-107">Per impostazione predefinita, Visual Basic passa i parametri per riferimento, come puntatori.</span><span class="sxs-lookup"><span data-stu-id="02ddf-107">By default, Visual Basic passes parameters by reference (as pointers).</span></span> <span data-ttu-id="02ddf-108">I parametri che devono essere passati solo per valore sono specificati dalla parola chiave **ByVal**.</span><span class="sxs-lookup"><span data-stu-id="02ddf-108">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span> <span data-ttu-id="02ddf-109">Un parametro **ByVal** â  **Integer** in Visual Basic, ad esempio, è equivalente a un parametro **short** in C++, mentre un parametro **ByRef** â  **Integer** in Visual Basic è equivalente a un parametro **short \*** .</span><span class="sxs-lookup"><span data-stu-id="02ddf-109">For example, a **ByVal** Â  **Integer** parameter in Visual Basic is equivalent to a **short** parameter in C++, whereas a **ByRef** Â  **Integer** parameter in Visual Basic is equivalent to a **short\*** parameter.</span></span>

<span data-ttu-id="02ddf-110">Un parametro dichiarato **come stringa** in Visual Basic viene dichiarato come puntatore a un **BSTR** in C++.</span><span class="sxs-lookup"><span data-stu-id="02ddf-110">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="02ddf-111">L'impostazione di un puntatore di stringa su **null** in C++ equivale a impostare la stringa sulla costante **vbNullString** in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="02ddf-111">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="02ddf-112">Il passaggio di una stringa di lunghezza zero ("") a una funzione progettata per la ricezione di **valori null** non funziona perché passa un puntatore a una stringa di lunghezza zero anziché a un puntatore zero.</span><span class="sxs-lookup"><span data-stu-id="02ddf-112">Passing a zero-length string ("") to a function designed to receive **NULL** does not work, because this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="02ddf-113">C++ e Visual Basic differiscono leggermente per la rappresentazione delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="02ddf-113">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="02ddf-114">In C++ le proprietà sono rappresentate come un set di funzioni di accesso, una che imposta il valore della proprietà e una che recupera il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="02ddf-114">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="02ddf-115">In Visual Basic le proprietà sono rappresentate come un singolo elemento che può essere utilizzato per recuperare o impostare il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="02ddf-115">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02ddf-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02ddf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02ddf-117">Conversione in C++</span><span class="sxs-lookup"><span data-stu-id="02ddf-117">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 




