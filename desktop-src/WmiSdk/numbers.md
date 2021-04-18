---
description: In MOF i numeri sono cifre che descrivono valori numerici. MOF fornisce un'ampia gamma di tipi di dati che si traducono in automazione e consente inoltre che tali numeri siano in formati diversi. Nella tabella seguente sono elencati i valori numerici supportati da MOF.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Numeri (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305575"
---
# <a name="numbers-wmi"></a><span data-ttu-id="974a4-105">Numeri (WMI)</span><span class="sxs-lookup"><span data-stu-id="974a4-105">Numbers (WMI)</span></span>

<span data-ttu-id="974a4-106">In MOF i numeri sono cifre che descrivono valori numerici.</span><span class="sxs-lookup"><span data-stu-id="974a4-106">In MOF, numbers are digits that describe numerical values.</span></span> <span data-ttu-id="974a4-107">MOF fornisce un'ampia gamma di tipi di dati che si traducono in automazione e consente inoltre che tali numeri siano in formati diversi.</span><span class="sxs-lookup"><span data-stu-id="974a4-107">MOF provides a variety of data types that translate into Automation, and also allows those numbers to be in different formats.</span></span> <span data-ttu-id="974a4-108">Nella tabella seguente sono elencati i valori numerici supportati da MOF.</span><span class="sxs-lookup"><span data-stu-id="974a4-108">The following table lists the numeric values that MOF supports.</span></span>



| <span data-ttu-id="974a4-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="974a4-109">Data type</span></span>  | <span data-ttu-id="974a4-110">Tipo di automazione</span><span class="sxs-lookup"><span data-stu-id="974a4-110">Automation type</span></span> | <span data-ttu-id="974a4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="974a4-111">Description</span></span>                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="974a4-112">**sint8**</span><span class="sxs-lookup"><span data-stu-id="974a4-112">**sint8**</span></span>  | <span data-ttu-id="974a4-113">**\_I2 VT**</span><span class="sxs-lookup"><span data-stu-id="974a4-113">**VT\_I2**</span></span>      | <span data-ttu-id="974a4-114">Signed Integer a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="974a4-114">Signed 8-bit integer.</span></span><br/>                                                                                                                                        |
| <span data-ttu-id="974a4-115">**sint16**</span><span class="sxs-lookup"><span data-stu-id="974a4-115">**sint16**</span></span> | <span data-ttu-id="974a4-116">**\_I2 VT**</span><span class="sxs-lookup"><span data-stu-id="974a4-116">**VT\_I2**</span></span>      | <span data-ttu-id="974a4-117">Intero con segno a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="974a4-117">Signed 16-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="974a4-118">**sint32**</span><span class="sxs-lookup"><span data-stu-id="974a4-118">**sint32**</span></span> | <span data-ttu-id="974a4-119">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="974a4-119">VT\_I4</span></span>          | <span data-ttu-id="974a4-120">Signed Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="974a4-120">Signed 32-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="974a4-121">**sint64**</span><span class="sxs-lookup"><span data-stu-id="974a4-121">**sint64**</span></span> | <span data-ttu-id="974a4-122">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="974a4-122">**VT\_BSTR**</span></span>    | <span data-ttu-id="974a4-123">Signed Integer a 64 bit in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="974a4-123">Signed 64-bit integer in string form.</span></span> <span data-ttu-id="974a4-124">Questo tipo segue il formato esadecimale o decimale in base alle regole del American National Standards Institute (ANSI) C.</span><span class="sxs-lookup"><span data-stu-id="974a4-124">This type follows hexadecimal or decimal format according to the American National Standards Institute (ANSI) C rules.</span></span><br/> |
| <span data-ttu-id="974a4-125">**real32**</span><span class="sxs-lookup"><span data-stu-id="974a4-125">**real32**</span></span> | <span data-ttu-id="974a4-126">**\_R4 VT**</span><span class="sxs-lookup"><span data-stu-id="974a4-126">**VT\_R4**</span></span>      | <span data-ttu-id="974a4-127">valore a virgola mobile a 4 byte che segue lo standard IEEE (Institute of Electrical and Electronics Engineers, Inc.).</span><span class="sxs-lookup"><span data-stu-id="974a4-127">4-byte floating-point value that follows the Institute of Electrical and Electronics Engineers, Inc. (IEEE) standard.</span></span><br/>                                        |
| <span data-ttu-id="974a4-128">**real64**</span><span class="sxs-lookup"><span data-stu-id="974a4-128">**real64**</span></span> | <span data-ttu-id="974a4-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="974a4-129">**VT\_R8**</span></span>      | <span data-ttu-id="974a4-130">valore a virgola mobile a 8 byte che segue lo standard IEEE.</span><span class="sxs-lookup"><span data-stu-id="974a4-130">8-byte floating-point value that follows the IEEE standard.</span></span><br/>                                                                                                  |
| <span data-ttu-id="974a4-131">**Uint8**</span><span class="sxs-lookup"><span data-stu-id="974a4-131">**uint8**</span></span>  | <span data-ttu-id="974a4-132">**\_Ui1 VT**</span><span class="sxs-lookup"><span data-stu-id="974a4-132">**VT\_UI1**</span></span>     | <span data-ttu-id="974a4-133">Intero senza segno a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="974a4-133">Unsigned 8-bit integer.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="974a4-134">**UInt16**</span><span class="sxs-lookup"><span data-stu-id="974a4-134">**uint16**</span></span> | <span data-ttu-id="974a4-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="974a4-135">**VT\_I4**</span></span>      | <span data-ttu-id="974a4-136">Intero senza segno a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="974a4-136">Unsigned 16-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="974a4-137">**uint32**</span><span class="sxs-lookup"><span data-stu-id="974a4-137">**uint32**</span></span> | <span data-ttu-id="974a4-138">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="974a4-138">**VT\_I4**</span></span>      | <span data-ttu-id="974a4-139">Intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="974a4-139">Unsigned 32-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="974a4-140">**uint64**</span><span class="sxs-lookup"><span data-stu-id="974a4-140">**uint64**</span></span> | <span data-ttu-id="974a4-141">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="974a4-141">**VT\_BSTR**</span></span>    | <span data-ttu-id="974a4-142">Intero senza segno a 64 bit in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="974a4-142">Unsigned 64-bit integer in string form.</span></span> <span data-ttu-id="974a4-143">Questo tipo segue il formato esadecimale o decimale secondo le regole ANSI C.</span><span class="sxs-lookup"><span data-stu-id="974a4-143">This type follows hexadecimal or decimal format according to ANSI C rules.</span></span><br/>                                           |



 

<span data-ttu-id="974a4-144">Sebbene il codice MOF flessibile riscontri alcune modifiche durante l'automazione:</span><span class="sxs-lookup"><span data-stu-id="974a4-144">Although flexible, MOF code does encounter some changes when dealing with Automation:</span></span>

-   <span data-ttu-id="974a4-145">È necessario codificare interi a 64 bit come stringhe.</span><span class="sxs-lookup"><span data-stu-id="974a4-145">You must encode 64-bit integers as strings.</span></span>

    <span data-ttu-id="974a4-146">L'automazione non supporta un tipo integrale a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="974a4-146">Automation does not support a 64-bit integral type.</span></span>

-   <span data-ttu-id="974a4-147">I tipi di automazione non sempre corrispondono alle dimensioni dei bit per i tipi di dati MOF.</span><span class="sxs-lookup"><span data-stu-id="974a4-147">Automation types do not always correspond in bit size to MOF data types.</span></span>

    <span data-ttu-id="974a4-148">Ad esempio, l'automazione USA VT \_ I4 per restituire un valore a 16 bit senza segno.</span><span class="sxs-lookup"><span data-stu-id="974a4-148">For example, Automation uses VT\_I4 to return an unsigned 16-bit value.</span></span> <span data-ttu-id="974a4-149">Questa discrepanza esiste a causa di problemi di estensione della firma.</span><span class="sxs-lookup"><span data-stu-id="974a4-149">This discrepancy exists because of sign-extension problems.</span></span> <span data-ttu-id="974a4-150">Se l'automazione usava VT \_ I2 anziché VT \_ I4, 65.536 sembrerebbe il valore 1, causando problemi di tipo e di intervallo.</span><span class="sxs-lookup"><span data-stu-id="974a4-150">If Automation used VT\_I2 instead of VT\_I4, 65,536 would appear to be the value  1, causing type and range problems.</span></span> <span data-ttu-id="974a4-151">Analogamente, l'automazione rappresenta il tipo **UInt32** come VT \_ I4 perché non esiste alcun tipo integer più grande che contenga **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="974a4-151">Similarly, Automation represents the **uint32** type as VT\_I4 because there exists no larger integer type to contain **uint32**.</span></span>

-   <span data-ttu-id="974a4-152">Non è necessario modificare alcuna rappresentazione per i tipi numerici a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="974a4-152">You do not need to change any representation for 8-bit numeral types.</span></span>

    <span data-ttu-id="974a4-153">L'automazione supporta VT \_ Ui1, un tipo senza segno a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="974a4-153">Automation supports VT\_UI1, an unsigned 8-bit type.</span></span>

<span data-ttu-id="974a4-154">MOF supporta costanti lunghe.</span><span class="sxs-lookup"><span data-stu-id="974a4-154">MOF supports long constants.</span></span> <span data-ttu-id="974a4-155">Viene dichiarata una costante lungo usando una semplice serie di cifre con un segno negativo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="974a4-155">You declare a long constant using a simple series of digits with an optional negative sign.</span></span> <span data-ttu-id="974a4-156">Una costante Long non può superare le dimensioni della variabile dichiarata in modo da contenerla.</span><span class="sxs-lookup"><span data-stu-id="974a4-156">A long constant cannot exceed the size of the variable that is declared to hold it.</span></span> <span data-ttu-id="974a4-157">Alcuni esempi di costanti lunghe sono 1000 e 12310.</span><span class="sxs-lookup"><span data-stu-id="974a4-157">Some examples of long constants are 1000 and  12310.</span></span>

<span data-ttu-id="974a4-158">MOF supporta inoltre formati numerici alternativi.</span><span class="sxs-lookup"><span data-stu-id="974a4-158">MOF also supports alternate numerical formats.</span></span> <span data-ttu-id="974a4-159">Nella tabella seguente sono elencati i caratteri speciali che è necessario utilizzare per descrivere le costanti esadecimali, binarie e ottali.</span><span class="sxs-lookup"><span data-stu-id="974a4-159">The following table lists the special characters you must use to describe hexadecimal, binary, and octal constants.</span></span>



| <span data-ttu-id="974a4-160">Costante</span><span class="sxs-lookup"><span data-stu-id="974a4-160">Constant</span></span>               | <span data-ttu-id="974a4-161">Carattere speciale</span><span class="sxs-lookup"><span data-stu-id="974a4-161">Special character</span></span>     | <span data-ttu-id="974a4-162">Esempio</span><span class="sxs-lookup"><span data-stu-id="974a4-162">Example</span></span>                   |
|------------------------|-----------------------|---------------------------|
| <span data-ttu-id="974a4-163">Decimal</span><span class="sxs-lookup"><span data-stu-id="974a4-163">Decimal</span></span><br/>     | <span data-ttu-id="974a4-164">nessuno</span><span class="sxs-lookup"><span data-stu-id="974a4-164">None</span></span><br/>       | <span data-ttu-id="974a4-165">Val = 65</span><span class="sxs-lookup"><span data-stu-id="974a4-165">val = 65</span></span><br/>       |
| <span data-ttu-id="974a4-166">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="974a4-166">Hexadecimal</span></span><br/> | <span data-ttu-id="974a4-167">prefisso 0x</span><span class="sxs-lookup"><span data-stu-id="974a4-167">0x prefix</span></span><br/>  | <span data-ttu-id="974a4-168">Val = 0x41</span><span class="sxs-lookup"><span data-stu-id="974a4-168">val = 0x41</span></span><br/>     |
| <span data-ttu-id="974a4-169">Ottale</span><span class="sxs-lookup"><span data-stu-id="974a4-169">Octal</span></span><br/>       | <span data-ttu-id="974a4-170">0 iniziali</span><span class="sxs-lookup"><span data-stu-id="974a4-170">Leading 0</span></span><br/>  | <span data-ttu-id="974a4-171">Val = 0101</span><span class="sxs-lookup"><span data-stu-id="974a4-171">val = 0101</span></span><br/>     |
| <span data-ttu-id="974a4-172">Binary</span><span class="sxs-lookup"><span data-stu-id="974a4-172">Binary</span></span><br/>      | <span data-ttu-id="974a4-173">Finali B</span><span class="sxs-lookup"><span data-stu-id="974a4-173">Trailing B</span></span><br/> | <span data-ttu-id="974a4-174">Val = 1000001B</span><span class="sxs-lookup"><span data-stu-id="974a4-174">val = 1000001B</span></span><br/> |



 

<span data-ttu-id="974a4-175">È possibile usare una costante a virgola mobile per rappresentare la notazione scientifica e le frazioni, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="974a4-175">You can use a floating-point constant to represent scientific notation as well as fractions, as shown next:</span></span>

``` syntax
3.14
-3.14
-1.2778E+02
```

<span data-ttu-id="974a4-176">WMI considera le costanti a virgola mobile come tipi di **VT \_ R8** per l'automazione.</span><span class="sxs-lookup"><span data-stu-id="974a4-176">WMI considers floating-point constants as **VT\_R8** types for Automation.</span></span>

<span data-ttu-id="974a4-177">Nell'esempio seguente vengono descritte le dichiarazioni di classe e istanza che illustrano come utilizzare ciascuno dei tipi di dati numerici per impostare le proprietà:</span><span class="sxs-lookup"><span data-stu-id="974a4-177">The following example describes class and instance declarations that illustrate how to use each of the numeric data types to set properties:</span></span>

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




