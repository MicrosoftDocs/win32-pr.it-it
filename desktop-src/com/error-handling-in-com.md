---
title: Gestione degli errori in COM (COM)
description: Gestione degli errori in COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104475010"
---
# <a name="error-handling-in-com-com"></a><span data-ttu-id="46985-103">Gestione degli errori in COM (COM)</span><span class="sxs-lookup"><span data-stu-id="46985-103">Error Handling in COM (COM)</span></span>

<span data-ttu-id="46985-104">Quasi tutte le funzioni COM e i metodi di interfaccia restituiscono un valore di tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="46985-104">Almost all COM functions and interface methods return a value of the type **HRESULT**.</span></span> <span data-ttu-id="46985-105">**HRESULT** (per *handle di risultato*) è un modo per restituire i valori di esito positivo, avviso ed errore.</span><span class="sxs-lookup"><span data-stu-id="46985-105">The **HRESULT** (for *result handle*) is a way of returning success, warning, and error values.</span></span> <span data-ttu-id="46985-106">Gli oggetti **HRESULT** s non sono effettivamente handle sono solo valori con diversi campi codificati nel valore.</span><span class="sxs-lookup"><span data-stu-id="46985-106">**HRESULT** s are really not handles to anything; they are only values with several fields encoded in the value.</span></span> <span data-ttu-id="46985-107">In base alla specifica COM, un risultato pari a zero indica un esito positivo e un risultato diverso da zero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="46985-107">As per the COM specification, a result of zero indicates success and a nonzero result indicates failure.</span></span>

<span data-ttu-id="46985-108">A livello di codice sorgente tutti i valori di errore sono costituiti da tre parti, separate da caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="46985-108">At the source code level, all error values consist of three parts, separated by underscores.</span></span> <span data-ttu-id="46985-109">La prima parte è il prefisso che identifica la struttura associata all'errore, la seconda parte è E per errore e la terza parte è una stringa che descrive la condizione effettiva.</span><span class="sxs-lookup"><span data-stu-id="46985-109">The first part is the prefix that identifies the facility associated with the error, the second part is E for error, and the third part is a string that describes the actual condition.</span></span> <span data-ttu-id="46985-110">Ad esempio, **STG \_ E \_ MEDIUMFULL** vengono restituiti quando non è disponibile spazio su disco rigido.</span><span class="sxs-lookup"><span data-stu-id="46985-110">For example, **STG\_E\_MEDIUMFULL** is returned when there is no space left on a hard disk.</span></span> <span data-ttu-id="46985-111">Il prefisso **STG** indica la funzionalità di archiviazione, **e** indica che il codice di stato rappresenta un errore e **MEDIUMFULL** fornisce informazioni specifiche sull'errore.</span><span class="sxs-lookup"><span data-stu-id="46985-111">The **STG** prefix indicates the storage facility, the **E** indicates that the status code represents an error, and the **MEDIUMFULL** provides specific information about the error.</span></span> <span data-ttu-id="46985-112">Molti dei valori che possono essere restituiti da una funzione o un metodo di interfaccia sono definiti in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="46985-112">Many of the values that you might want to return from an interface method or function are defined in Winerror.h.</span></span>

<span data-ttu-id="46985-113">Per ulteriori informazioni sulla gestione degli errori, vedere le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="46985-113">For more information about error handling, see the following sections:</span></span>

-   [<span data-ttu-id="46985-114">Struttura dei codici di errore COM</span><span class="sxs-lookup"><span data-stu-id="46985-114">Structure of COM Error Codes</span></span>](structure-of-com-error-codes.md)
-   [<span data-ttu-id="46985-115">Codici in funzionalità \_ ITF</span><span class="sxs-lookup"><span data-stu-id="46985-115">Codes in FACILITY\_ITF</span></span>](codes-in-facility-itf.md)
-   [<span data-ttu-id="46985-116">Uso delle macro per la gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="46985-116">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
-   [<span data-ttu-id="46985-117">Gestione degli errori COM in Java e Visual Basic</span><span class="sxs-lookup"><span data-stu-id="46985-117">COM Error Handling in Java and Visual Basic</span></span>](com-error-handling-in-java-and-visual-basic.md)
-   [<span data-ttu-id="46985-118">Strategie di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="46985-118">Error Handling Strategies</span></span>](error-handling-strategies.md)
-   [<span data-ttu-id="46985-119">Gestione degli errori sconosciuti</span><span class="sxs-lookup"><span data-stu-id="46985-119">Handling Unknown Errors</span></span>](handling-unknown-errors.md)

## <a name="related-topics"></a><span data-ttu-id="46985-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46985-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46985-121">Codici di errore COM</span><span class="sxs-lookup"><span data-stu-id="46985-121">COM Error Codes</span></span>](com-error-codes.md)
</dt> </dl>

 

 




