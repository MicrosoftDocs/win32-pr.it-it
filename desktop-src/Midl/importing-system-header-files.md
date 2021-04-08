---
title: Importazione di file di intestazione di sistema
description: Sebbene sia spesso possibile utilizzare la direttiva \ include per includere i file di intestazione nel file IDL, non è consigliabile.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importazione di MIDL, file di intestazione di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761590"
---
# <a name="importing-system-header-files"></a><span data-ttu-id="99a67-104">Importazione di file di intestazione di sistema</span><span class="sxs-lookup"><span data-stu-id="99a67-104">Importing System Header Files</span></span>

<span data-ttu-id="99a67-105">Sebbene sia spesso possibile utilizzare la direttiva **\# include** per includere i file di intestazione nel file IDL, non è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="99a67-105">While it is often possible to use the **\#include** directive to include header files in your IDL file, it is not recommended.</span></span> <span data-ttu-id="99a67-106">Il compilatore MIDL genererà gli stub per tutte le funzioni definite nel file IDL da compilare.</span><span class="sxs-lookup"><span data-stu-id="99a67-106">The MIDL compiler will generate stubs for all functions defined in the IDL file being compiled.</span></span> <span data-ttu-id="99a67-107">In genere, un file di intestazione contiene un numero di prototipi che non è necessario né includere nei file stub e un' **\# inclusione** inserisce efficacemente tutte le definizioni nel file IDL principale.</span><span class="sxs-lookup"><span data-stu-id="99a67-107">Usually a header file contains a number of prototypes that you neither need nor want to include in your stub files, and a **\#include** effectively puts all those definitions into your main IDL file.</span></span> <span data-ttu-id="99a67-108">Inoltre, se nel file di intestazione sono definiti tipi non, il file IDL potrebbe non essere compilato.</span><span class="sxs-lookup"><span data-stu-id="99a67-108">Furthermore, if there are nonremotable types defined in the header file, the IDL file may not compile.</span></span>

<span data-ttu-id="99a67-109">Esistono due modi per includere le definizioni dei tipi dai file di intestazione in un file IDL:</span><span class="sxs-lookup"><span data-stu-id="99a67-109">There are two ways to include type definitions from header files in an IDL file:</span></span>

-   <span data-ttu-id="99a67-110">Utilizzare la direttiva [**Import**](import.md) per includere i tipi di dati definiti in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="99a67-110">Use the [**import**](import.md) directive to include data types defined in a header file.</span></span> <span data-ttu-id="99a67-111">A differenza della direttiva di **\# inclusione** del linguaggio C, la direttiva **Import** preleva solo le definizioni di tipo e costante e ignora i prototipi di procedura.</span><span class="sxs-lookup"><span data-stu-id="99a67-111">Unlike the C-language **\#include** directive, the **import** directive only picks up type and constant definitions and ignores procedure prototypes.</span></span> <span data-ttu-id="99a67-112">Questo approccio funzionerà purché il file IDL principale non faccia riferimento ad alcun tipo non definito nel file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="99a67-112">This approach will work as long as your main IDL file does not reference any nonremotable types defined in the header file.</span></span>
-   <span data-ttu-id="99a67-113">Creare un file IDL helper con un'interfaccia fittizia che includa i file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="99a67-113">Create a helper IDL file with a dummy interface that includes the header files.</span></span> <span data-ttu-id="99a67-114">Usare quindi la direttiva [**Import**](import.md) per includere il file helper.</span><span class="sxs-lookup"><span data-stu-id="99a67-114">Then, use the [**import**](import.md) directive to include the helper file.</span></span> <span data-ttu-id="99a67-115">In questo modo, solo i [**typedef**](typedef.md)verranno visualizzati negli Stub compilati.</span><span class="sxs-lookup"><span data-stu-id="99a67-115">In this way, only the [**typedef**](typedef.md)s will appear in the compiled stubs.</span></span> <span data-ttu-id="99a67-116">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="99a67-116">For example:</span></span>

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
