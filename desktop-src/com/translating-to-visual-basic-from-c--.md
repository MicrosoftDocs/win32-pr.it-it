---
title: Conversione in Visual Basic da C++
description: Conversione in Visual Basic da C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298423"
---
# <a name="translating-to-visual-basic-from-c"></a><span data-ttu-id="2b15d-103">Conversione in Visual Basic da C++</span><span class="sxs-lookup"><span data-stu-id="2b15d-103">Translating to Visual Basic from C++</span></span>

<span data-ttu-id="2b15d-104">Utilizzando il linguaggio di programmazione C++, gli sviluppatori possono accedere direttamente alla memoria che archivia una determinata variabile.</span><span class="sxs-lookup"><span data-stu-id="2b15d-104">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="2b15d-105">I puntatori alla memoria forniscono questo accesso diretto.</span><span class="sxs-lookup"><span data-stu-id="2b15d-105">Memory pointers provide this direct access.</span></span> <span data-ttu-id="2b15d-106">In Visual Basic, i puntatori vengono gestiti per l'utente.</span><span class="sxs-lookup"><span data-stu-id="2b15d-106">In Visual Basic, pointers are handled for you.</span></span> <span data-ttu-id="2b15d-107">Un parametro dichiarato come puntatore a **int** in C++, ad esempio, è equivalente a un parametro dichiarato in Visual Basic come un integer **ByRef** \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="2b15d-107">For example, a parameter declared as a pointer to an **int** in C++ is equivalent to a parameter declared in Visual Basic as a **ByRef** **Integer**.</span></span>

<span data-ttu-id="2b15d-108">Un parametro dichiarato **come stringa** in Visual Basic viene dichiarato come puntatore a un **BSTR** in C++.</span><span class="sxs-lookup"><span data-stu-id="2b15d-108">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="2b15d-109">L'impostazione di un puntatore di stringa su **null** in C++ equivale a impostare la stringa sulla costante **vbNullString** in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2b15d-109">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="2b15d-110">Il passaggio di una stringa di lunghezza zero ("") a una funzione progettata per la ricezione di **valori null** non funziona, poiché viene passato un puntatore a una stringa di lunghezza zero anziché a un puntatore zero.</span><span class="sxs-lookup"><span data-stu-id="2b15d-110">Passing in a zero-length string ("") to a function designed to receive **NULL** does not work, as this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="2b15d-111">C++ supporta i contenitori di dati, ovvero le strutture e le unioni, che non hanno equivalenti nelle prime versioni di Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2b15d-111">C++ supports data containers, namely structures and unions, that have no equivalent in early versions of Visual Basic.</span></span> <span data-ttu-id="2b15d-112">Per questo motivo, gli oggetti COM in genere incapsulano informazioni che in genere sono archiviate in strutture e unioni nelle classi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="2b15d-112">For this reason, COM objects typically wrap information that usually is stored in structures and unions in object classes.</span></span> <span data-ttu-id="2b15d-113">Alcuni oggetti COM, tuttavia, possono contenere strutture, causando la inaccessibilità di parti dei metodi o delle funzionalità dell'oggetto per Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2b15d-113">Some COM objects, however, may contain structures, causing portions of the object's methods or functionality to be inaccessible to Visual Basic.</span></span>

<span data-ttu-id="2b15d-114">Alcuni tipi di dati C++ non sono supportati in Visual Basic, ad esempio tipi senza segno e tipi **HWND** .</span><span class="sxs-lookup"><span data-stu-id="2b15d-114">Some C++ data types are not supported in Visual Basic, for example unsigned types and **HWND** types.</span></span> <span data-ttu-id="2b15d-115">I metodi che accettano o restituiscono questi tipi di dati non sono disponibili in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2b15d-115">Methods that accept or return these data types are not available in Visual Basic.</span></span>

<span data-ttu-id="2b15d-116">Visual Basic usa tipi di dati compatibili con l'automazione come tipi di dati interni.</span><span class="sxs-lookup"><span data-stu-id="2b15d-116">Visual Basic uses Automation-compatible data types as its internal data types.</span></span> <span data-ttu-id="2b15d-117">I tipi di dati C++ compatibili con l'automazione sono pertanto compatibili anche con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2b15d-117">Thus, C++ data types that are Automation-compatible are also compatible with Visual Basic.</span></span> <span data-ttu-id="2b15d-118">I tipi di dati che non sono compatibili con l'automazione potrebbero non essere in grado di essere convertiti in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2b15d-118">Data types that are not Automation-compatible may not be able to be converted to Visual Basic.</span></span>

<span data-ttu-id="2b15d-119">Nella tabella seguente sono elencati i tipi di dati supportati da Visual Basic e dai rispettivi equivalenti **VarType** .</span><span class="sxs-lookup"><span data-stu-id="2b15d-119">The following table lists the data types are supported by Visual Basic and their **VARTYPE** equivalents.</span></span> <span data-ttu-id="2b15d-120">**VarType** è un'enumerazione che elenca i tipi Variant di automazione.</span><span class="sxs-lookup"><span data-stu-id="2b15d-120">**VARTYPE** is an enumeration that lists the Automation variant types.</span></span>



| <span data-ttu-id="2b15d-121">Tipo di dati di Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2b15d-121">Visual Basic data type</span></span>  | <span data-ttu-id="2b15d-122">Equivalente VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2b15d-122">VARTYPE equivalent</span></span>                |
|-------------------------|-----------------------------------|
| <span data-ttu-id="2b15d-123">**Integer**</span><span class="sxs-lookup"><span data-stu-id="2b15d-123">**Integer**</span></span><br/>  | <span data-ttu-id="2b15d-124">16 bit, firmato, VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="2b15d-124">16 bit, signed, VT\_I2</span></span><br/> |
| <span data-ttu-id="2b15d-125">**Long**</span><span class="sxs-lookup"><span data-stu-id="2b15d-125">**Long**</span></span><br/>     | <span data-ttu-id="2b15d-126">32 bit, firmato, VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2b15d-126">32 bit, signed, VT\_I4</span></span><br/> |
| <span data-ttu-id="2b15d-127">**Data**</span><span class="sxs-lookup"><span data-stu-id="2b15d-127">**Date**</span></span><br/>     | <span data-ttu-id="2b15d-128">\_Data VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-128">VT\_DATE</span></span><br/>               |
| <span data-ttu-id="2b15d-129">**Valuta**</span><span class="sxs-lookup"><span data-stu-id="2b15d-129">**Currency**</span></span><br/> | <span data-ttu-id="2b15d-130">\_CY VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-130">VT\_CY</span></span><br/>                 |
| <span data-ttu-id="2b15d-131">**Object**</span><span class="sxs-lookup"><span data-stu-id="2b15d-131">**Object**</span></span><br/>   | <span data-ttu-id="2b15d-132">\*\_invio VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-132">\*VT\_DISPATCH</span></span><br/>         |
| <span data-ttu-id="2b15d-133">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="2b15d-133">**String**</span></span><br/>   | <span data-ttu-id="2b15d-134">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-134">VT\_BSTR</span></span><br/>               |
| <span data-ttu-id="2b15d-135">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b15d-135">**Boolean**</span></span><br/>  | <span data-ttu-id="2b15d-136">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-136">VT\_BOOL</span></span><br/>               |
| <span data-ttu-id="2b15d-137">**Valuta**</span><span class="sxs-lookup"><span data-stu-id="2b15d-137">**Currency**</span></span><br/> | <span data-ttu-id="2b15d-138">\_decimale VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-138">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="2b15d-139">**Singolo**</span><span class="sxs-lookup"><span data-stu-id="2b15d-139">**Single**</span></span><br/>   | <span data-ttu-id="2b15d-140">\_R4 VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-140">VT\_R4</span></span><br/>                 |
| <span data-ttu-id="2b15d-141">**Double**</span><span class="sxs-lookup"><span data-stu-id="2b15d-141">**Double**</span></span><br/>   | <span data-ttu-id="2b15d-142">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="2b15d-142">VT\_R8</span></span><br/>                 |
| <span data-ttu-id="2b15d-143">**Decimale**</span><span class="sxs-lookup"><span data-stu-id="2b15d-143">**Decimal**</span></span><br/>  | <span data-ttu-id="2b15d-144">\_decimale VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-144">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="2b15d-145">**Byte**</span><span class="sxs-lookup"><span data-stu-id="2b15d-145">**Byte**</span></span><br/>     | <span data-ttu-id="2b15d-146">\_decimale VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-146">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="2b15d-147">**Variante**</span><span class="sxs-lookup"><span data-stu-id="2b15d-147">**Variant**</span></span><br/>  | <span data-ttu-id="2b15d-148">\_variante VT</span><span class="sxs-lookup"><span data-stu-id="2b15d-148">VT\_VARIANT</span></span><br/>            |



 

<span data-ttu-id="2b15d-149">Tutti i parametri in Visual Basic, a meno che non siano contrassegnati con la parola chiave **ByVal**, vengono passati per riferimento (come puntatori) anziché per valore.</span><span class="sxs-lookup"><span data-stu-id="2b15d-149">All parameters in Visual Basic, unless labeled with the keyword **ByVal**, are passed by reference (as pointers) instead of by value.</span></span>

<span data-ttu-id="2b15d-150">C++ e Visual Basic differiscono leggermente per la rappresentazione delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b15d-150">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="2b15d-151">In C++ le proprietà sono rappresentate come un set di funzioni di accesso, una che imposta il valore della proprietà e una che recupera il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b15d-151">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="2b15d-152">In Visual Basic le proprietà sono rappresentate come un singolo elemento che può essere utilizzato per recuperare o impostare il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b15d-152">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b15d-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b15d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b15d-154">Conversione in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2b15d-154">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 





