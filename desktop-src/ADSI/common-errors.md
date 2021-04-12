---
title: Errori comuni (ADSI)
description: Tutti gli errori specifici di ADSI hanno un formato esadecimale di 80005xxx. I codici di errore più comuni rilevati sono descritti nella tabella seguente.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "104335988"
---
# <a name="common-errors-adsi"></a><span data-ttu-id="da8fe-104">Errori comuni (ADSI)</span><span class="sxs-lookup"><span data-stu-id="da8fe-104">Common Errors (ADSI)</span></span>

<span data-ttu-id="da8fe-105">Tutti gli errori specifici di ADSI hanno un formato esadecimale di 80005xxx.</span><span class="sxs-lookup"><span data-stu-id="da8fe-105">All ADSI-specific errors have a hexadecimal form of 80005xxx.</span></span> <span data-ttu-id="da8fe-106">I codici di errore più comuni rilevati sono descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="da8fe-106">The most common error codes encountered are outlined in the following table.</span></span>



| <span data-ttu-id="da8fe-107">Codice errore esadecimale ADSI</span><span class="sxs-lookup"><span data-stu-id="da8fe-107">ADSI hex error code</span></span> | <span data-ttu-id="da8fe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da8fe-108">Description</span></span>                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da8fe-109">80005000</span><span class="sxs-lookup"><span data-stu-id="da8fe-109">80005000</span></span><br/> | <span data-ttu-id="da8fe-110">È stato passato un percorso ADSI non valido.</span><span class="sxs-lookup"><span data-stu-id="da8fe-110">An invalid ADSI pathname was passed.</span></span> <span data-ttu-id="da8fe-111">Questo errore deriva dal passaggio di un ADsPath in formato non corretto a **GetObject** durante l'associazione a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="da8fe-111">This error results from passing a poorly formed ADsPath to **GetObject** when binding to an object.</span></span><br/> |
| <span data-ttu-id="da8fe-112">8000500D</span><span class="sxs-lookup"><span data-stu-id="da8fe-112">8000500D</span></span><br/> | <span data-ttu-id="da8fe-113">La proprietà ADSI non è stata trovata nella cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="da8fe-113">The ADSI property cannot be found in the property cache.</span></span><br/>                                                                                 |
| <span data-ttu-id="da8fe-114">8000500E</span><span class="sxs-lookup"><span data-stu-id="da8fe-114">8000500E</span></span><br/> | <span data-ttu-id="da8fe-115">L'oggetto ADSI esiste.</span><span class="sxs-lookup"><span data-stu-id="da8fe-115">The ADSI object exists.</span></span> <span data-ttu-id="da8fe-116">Questo errore si verificherà se si tenta di creare un oggetto ADSI con lo stesso nome di un oggetto ADSI esistente.</span><span class="sxs-lookup"><span data-stu-id="da8fe-116">If you attempt to create an ADSI object with the same name as an existing ADSI object, this error will occur.</span></span><br/>    |



 

<span data-ttu-id="da8fe-117">Per un elenco completo dei codici di errore ADSI, vedere [codici di errore ADSI generici](generic-adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="da8fe-117">For a complete list of ADSI error codes, see [Generic ADSI Error Codes](generic-adsi-error-codes.md).</span></span>

## <a name="com-errors"></a><span data-ttu-id="da8fe-118">Errori COM</span><span class="sxs-lookup"><span data-stu-id="da8fe-118">COM Errors</span></span>

<span data-ttu-id="da8fe-119">Poiché ADSI è costituito da oggetti COM, restituirà codici di errore COM standard.</span><span class="sxs-lookup"><span data-stu-id="da8fe-119">Since ADSI is composed of COM objects, it will return standard COM error codes.</span></span> <span data-ttu-id="da8fe-120">Nella tabella seguente sono elencati i codici di errore COM più comunemente rilevati nella programmazione ADSI.</span><span class="sxs-lookup"><span data-stu-id="da8fe-120">The following table lists the COM error codes most commonly encountered in ADSI programming.</span></span>



| <span data-ttu-id="da8fe-121">Codice errore esadecimale COM</span><span class="sxs-lookup"><span data-stu-id="da8fe-121">COM hex error code</span></span>  | <span data-ttu-id="da8fe-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da8fe-122">Description</span></span>                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da8fe-123">80004005</span><span class="sxs-lookup"><span data-stu-id="da8fe-123">80004005</span></span><br/> | <span data-ttu-id="da8fe-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="da8fe-124">Unspecified error.</span></span> <span data-ttu-id="da8fe-125">La cause dell'errore dell'oggetto COM è indeterminata da ADSI.</span><span class="sxs-lookup"><span data-stu-id="da8fe-125">The cause of the COM object failure is indeterminate by ADSI.</span></span> <br/>                                  |
| <span data-ttu-id="da8fe-126">800041E4</span><span class="sxs-lookup"><span data-stu-id="da8fe-126">800041E4</span></span><br/> | <span data-ttu-id="da8fe-127">Oggetto non trovato.</span><span class="sxs-lookup"><span data-stu-id="da8fe-127">Object not found.</span></span> <span data-ttu-id="da8fe-128">Questo errore si verifica principalmente a causa dell'errore di ortografia della stringa ADsPath durante l'associazione a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="da8fe-128">This error predominantly occurs due to misspelling the ADsPath string when binding to an object.</span></span><br/> |



 

<span data-ttu-id="da8fe-129">Vedere [codici di errore com generici](generic-com-error-codes.md) per altri esempi di errori com che possono verificarsi nella programmazione ADSI.</span><span class="sxs-lookup"><span data-stu-id="da8fe-129">See [Generic COM Error Codes](generic-com-error-codes.md) for a few more examples of COM errors that may occur in ADSI programming.</span></span>

## <a name="win32-errors"></a><span data-ttu-id="da8fe-130">Errori Win32</span><span class="sxs-lookup"><span data-stu-id="da8fe-130">Win32 Errors</span></span>

<span data-ttu-id="da8fe-131">Qualsiasi codice di errore del formato esadecimale 8007xxxx è un codice di errore Win32 standard.</span><span class="sxs-lookup"><span data-stu-id="da8fe-131">Any error code of the hexadecimal form 8007xxxx is a standard Win32 error code.</span></span> <span data-ttu-id="da8fe-132">Se si convertono le ultime quattro cifre da esadecimali a decimali, è possibile accedere all'errore dalla riga di comando di Windows 2000:</span><span class="sxs-lookup"><span data-stu-id="da8fe-132">If you convert the last four digits from hexadecimal to decimal, you can access the error from the Windows 2000 command line:</span></span>

<span data-ttu-id="da8fe-133">**helpmsg NET <number>**</span><span class="sxs-lookup"><span data-stu-id="da8fe-133">**net helpmsg <number>**</span></span>

<span data-ttu-id="da8fe-134">Nella riga di comando precedente, " &lt; Number &gt; " è il numero decimale ottenuto convertendo le ultime quattro cifre del codice di errore da esadecimale.</span><span class="sxs-lookup"><span data-stu-id="da8fe-134">In the command line above, "&lt;number&gt;" is the decimal number obtained by converting the last four digits of the error code from hexadecimal.</span></span> <span data-ttu-id="da8fe-135">Questa riga di comando fornirà una descrizione più utile dell'errore Win32, che può essere molto utile per il debug dello script.</span><span class="sxs-lookup"><span data-stu-id="da8fe-135">This command line will provide a more useful description of the Win32 error, which can be of great help in debugging your script.</span></span>

 

 





