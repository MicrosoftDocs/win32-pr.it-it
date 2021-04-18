---
description: ICE70 verifica che i valori integer per le voci del registro di sistema siano specificati correttamente.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315469"
---
# <a name="ice70"></a><span data-ttu-id="cfba8-103">ICE70</span><span class="sxs-lookup"><span data-stu-id="cfba8-103">ICE70</span></span>

<span data-ttu-id="cfba8-104">ICE70 verifica che i valori integer per le voci del registro di sistema siano specificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="cfba8-104">ICE70 verifies that integer values for registry entries are specified correctly.</span></span> <span data-ttu-id="cfba8-105">I valori nel formato \# \# Str, \# % unexpanded Str non vengono convalidati.</span><span class="sxs-lookup"><span data-stu-id="cfba8-105">Values of the form \#\#str, \#%unexpanded str are not validated.</span></span> <span data-ttu-id="cfba8-106">\#Vengono convalidati i valori nel formato xhex, \# xhex, \# Integer e \# \[ Property \] .</span><span class="sxs-lookup"><span data-stu-id="cfba8-106">Values of the form \#xhex, \#Xhex, \#integer, and \#\[property\] are validated.</span></span> <span data-ttu-id="cfba8-107">La tabella seguente fornisce una breve panoramica.</span><span class="sxs-lookup"><span data-stu-id="cfba8-107">The following table provides a brief overview.</span></span>



| <span data-ttu-id="cfba8-108">Valore</span><span class="sxs-lookup"><span data-stu-id="cfba8-108">Value</span></span>                 | <span data-ttu-id="cfba8-109">Convalida</span><span class="sxs-lookup"><span data-stu-id="cfba8-109">Validation</span></span>                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="cfba8-110">\#\#Str</span><span class="sxs-lookup"><span data-stu-id="cfba8-110">\#\#str</span></span>               | <span data-ttu-id="cfba8-111">valido</span><span class="sxs-lookup"><span data-stu-id="cfba8-111">valid</span></span>                                                                         |
| <span data-ttu-id="cfba8-112">\#% Str non espansa</span><span class="sxs-lookup"><span data-stu-id="cfba8-112">\#%unexpanded str</span></span>     | <span data-ttu-id="cfba8-113">valido</span><span class="sxs-lookup"><span data-stu-id="cfba8-113">valid</span></span>                                                                         |
| <span data-ttu-id="cfba8-114">\#xHex, \# xHex</span><span class="sxs-lookup"><span data-stu-id="cfba8-114">\#xHex,\#XHex</span></span>         | <span data-ttu-id="cfba8-115">Verificare la presenza di caratteri esadecimali validi (da 0 a 9, a-f, A-F).</span><span class="sxs-lookup"><span data-stu-id="cfba8-115">Validate for valid hex characters (0-9,a-f,A-F).</span></span> <span data-ttu-id="cfba8-116">Le proprietà sono consentite qui.</span><span class="sxs-lookup"><span data-stu-id="cfba8-116">Properties are allowed here.</span></span> |
| <span data-ttu-id="cfba8-117">\#+ int, \# -int, \# int</span><span class="sxs-lookup"><span data-stu-id="cfba8-117">\#+int, \#-int, \#int</span></span> | <span data-ttu-id="cfba8-118">Verificare la presenza di caratteri numerici validi (0-9).</span><span class="sxs-lookup"><span data-stu-id="cfba8-118">Validate for valid numeric characters (0-9).</span></span> <span data-ttu-id="cfba8-119">Le proprietà sono consentite qui.</span><span class="sxs-lookup"><span data-stu-id="cfba8-119">Properties are allowed here.</span></span>     |



 

<span data-ttu-id="cfba8-120">La sintassi per un valore integer da immettere nel registro di sistema è \# Integer in cui Integer è numerico.</span><span class="sxs-lookup"><span data-stu-id="cfba8-120">The syntax for an integer value to be entered into the registry is \#integer where integer is numerical.</span></span>

## <a name="result"></a><span data-ttu-id="cfba8-121">Risultato</span><span class="sxs-lookup"><span data-stu-id="cfba8-121">Result</span></span>

<span data-ttu-id="cfba8-122">ICE70 segnala un errore se i valori integer per le voci del registro di sistema non sono specificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="cfba8-122">ICE70 reports an error if integer values for registry entries are not specified correctly.</span></span>

## <a name="example"></a><span data-ttu-id="cfba8-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="cfba8-123">Example</span></span>

<span data-ttu-id="cfba8-124">ICE70 segnala gli errori seguenti per l'esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="cfba8-124">ICE70 reports the following errors for the given example.</span></span>

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

<span data-ttu-id="cfba8-125">Per correggere l'errore: se si desidera che il valore sia numerico, modificare il valore in modo da utilizzare tutti i caratteri numerici.</span><span class="sxs-lookup"><span data-stu-id="cfba8-125">To fix this error: If you want the value to be numeric, change the value to use all numeric characters.</span></span> <span data-ttu-id="cfba8-126">Se si desidera che il valore sia una stringa, deve essere preceduto da due ' \# ' ( \# \# ) anziché uno solo.</span><span class="sxs-lookup"><span data-stu-id="cfba8-126">If you want the value to be a string, it must be preceded by two '\#' (\#\#) instead of just one.</span></span>

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

<span data-ttu-id="cfba8-127">Per correggere l'errore: i caratteri esadecimali validi sono 0-9, A-F e a-f.</span><span class="sxs-lookup"><span data-stu-id="cfba8-127">To fix this error: Valid hexadecimal characters are 0-9, A-F, and a-f.</span></span> <span data-ttu-id="cfba8-128">Solo questi caratteri possono seguire la \# x (o \# x).</span><span class="sxs-lookup"><span data-stu-id="cfba8-128">Only these characters can follow the \#x (or \#X).</span></span>

<span data-ttu-id="cfba8-129">[Tabella del registro di sistema](registry-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="cfba8-129">[Registry table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="cfba8-130">Registro</span><span class="sxs-lookup"><span data-stu-id="cfba8-130">Registry</span></span> | <span data-ttu-id="cfba8-131">Valore</span><span class="sxs-lookup"><span data-stu-id="cfba8-131">Value</span></span>    |
|----------|----------|
| <span data-ttu-id="cfba8-132">Reg1</span><span class="sxs-lookup"><span data-stu-id="cfba8-132">Reg1</span></span>     | <span data-ttu-id="cfba8-133">\#12xz34</span><span class="sxs-lookup"><span data-stu-id="cfba8-133">\#12xz34</span></span> |
| <span data-ttu-id="cfba8-134">Reg2</span><span class="sxs-lookup"><span data-stu-id="cfba8-134">Reg2</span></span>     | <span data-ttu-id="cfba8-135">\#xz34</span><span class="sxs-lookup"><span data-stu-id="cfba8-135">\#xz34</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="cfba8-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfba8-136">Remarks</span></span>

-   <span data-ttu-id="cfba8-137">\#\[proprietà \] valida.</span><span class="sxs-lookup"><span data-stu-id="cfba8-137">\#\[myproperty\] is valid.</span></span>
-   <span data-ttu-id="cfba8-138">\#\[Proprietà non valida (parentesi di chiusura mancante).</span><span class="sxs-lookup"><span data-stu-id="cfba8-138">\#\[myproperty is not valid (missing ending bracket).</span></span>
-   <span data-ttu-id="cfba8-139">\#\[\] \[ myprop2 myprop1 è valido.</span><span class="sxs-lookup"><span data-stu-id="cfba8-139">\#\[myprop1\] \[myprop2 is valid.</span></span> <span data-ttu-id="cfba8-140">(Anche se l'ultimo manca la parentesi finale, myprop1 potrebbe restituire Str, in \# modo da avere \# \# Str \[ myprop2, che è valido</span><span class="sxs-lookup"><span data-stu-id="cfba8-140">(Even though the last one is missing the ending bracket, myprop1 could evaluate to \#str so you would have \#\#str \[myprop2, which is valid</span></span>
-   <span data-ttu-id="cfba8-141">\#\]proprietà \[ non valida</span><span class="sxs-lookup"><span data-stu-id="cfba8-141">\#\]myproperty\[ is not valid</span></span>
-   <span data-ttu-id="cfba8-142">Qualsiasi proprietà incorporata in una stringa valore non può trovarsi nel \[ \] form $compkey, \[ \# FileKey \] o \[ ! FileKey \] perché non sono numerici.</span><span class="sxs-lookup"><span data-stu-id="cfba8-142">Any embedded property in a value string cannot be in \[$compkey\], \[\#filekey\], or \[!filekey\] form because these are not numeric.</span></span> <span data-ttu-id="cfba8-143">Tuttavia, esiste un'eccezione, la \# \[ proprietà \] \[ $compkey \] (o \[ \# FileKey \] o \[ ! FileKey \] ) è valida perché, come nel precedente, la \[ proprietà \] può restituire \# Str.</span><span class="sxs-lookup"><span data-stu-id="cfba8-143">However, there is one exception, \#\[myproperty\] \[$compkey\] (or \[\#filekey\] or \[!filekey\]) is valid because, as with the preceding, \[myproperty\] can evaluate to \#str.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfba8-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfba8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfba8-145">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="cfba8-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



