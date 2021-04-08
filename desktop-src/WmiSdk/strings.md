---
title: Stringhe MOF
description: Una stringa è un tipo di dati che contiene una stringa di caratteri generalmente intesa come testo leggibile.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880438"
---
# <a name="mof-strings"></a><span data-ttu-id="8dfe8-103">Stringhe MOF</span><span class="sxs-lookup"><span data-stu-id="8dfe8-103">MOF strings</span></span>

<span data-ttu-id="8dfe8-104">Una stringa è un tipo di dati che contiene una stringa di caratteri generalmente intesa come testo leggibile.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-104">A string is a data type that contains a string of characters usually intended as human-readable text.</span></span> <span data-ttu-id="8dfe8-105">MOF descrive due tipi di stringhe, che usano per ospitare uno o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-105">MOF describes two types of strings, which use to hold single or multiple characters.</span></span> <span data-ttu-id="8dfe8-106">MOF dispone inoltre di una serie di regole che descrivono l'utilizzo delle virgolette all'interno di una stringa.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-106">MOF also has a series of rules describing the use of quotes within a string.</span></span>

<span data-ttu-id="8dfe8-107">Nella tabella seguente sono elencati i tipi di dati stringa per MOF.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-107">The following table lists the string data types for MOF.</span></span>



| <span data-ttu-id="8dfe8-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8dfe8-108">Data type</span></span>  | <span data-ttu-id="8dfe8-109">Tipo di automazione</span><span class="sxs-lookup"><span data-stu-id="8dfe8-109">Automation type</span></span> | <span data-ttu-id="8dfe8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dfe8-110">Description</span></span>                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfe8-111">**char16**</span><span class="sxs-lookup"><span data-stu-id="8dfe8-111">**char16**</span></span> | <span data-ttu-id="8dfe8-112">**\_I2 VT**</span><span class="sxs-lookup"><span data-stu-id="8dfe8-112">**VT\_I2**</span></span>      | <span data-ttu-id="8dfe8-113">Singolo carattere Unicode a 16 bit nel formato 2 (UCS-2) del set di caratteri universali</span><span class="sxs-lookup"><span data-stu-id="8dfe8-113">Single 16-bit Unicode character in Universal Character Set 2 (UCS-2) format</span></span><br/> |
| <span data-ttu-id="8dfe8-114">**string**</span><span class="sxs-lookup"><span data-stu-id="8dfe8-114">**string**</span></span> | <span data-ttu-id="8dfe8-115">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="8dfe8-115">**VT\_BSTR**</span></span>    | <span data-ttu-id="8dfe8-116">Stringa di caratteri Unicode</span><span class="sxs-lookup"><span data-stu-id="8dfe8-116">Unicode character string</span></span><br/>                                                    |



 

<span data-ttu-id="8dfe8-117">Usare le linee guida seguenti per la scrittura di stringhe per MOF:</span><span class="sxs-lookup"><span data-stu-id="8dfe8-117">Use the following guidelines when writing strings for MOF:</span></span>

-   <span data-ttu-id="8dfe8-118">Racchiudere le costanti a carattere singolo con virgolette singole.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-118">Surround single-character constants with single quotes.</span></span>

    <span data-ttu-id="8dfe8-119">Se non si utilizzano virgolette singole con costanti carattere singolo, è necessario utilizzare la rappresentazione Integer del valore del carattere Unicode.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-119">If you do not use single quotes with single character constants, you must use the integer representation of the Unicode character value.</span></span> <span data-ttu-id="8dfe8-120">Facoltativamente, è possibile specificare il carattere letteralmente con la \\ sequenza di escape x dello standard American National Standards Institute (ANSI) C, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="8dfe8-120">Optionally, you could specify the character literally with the \\x escape sequence from the American National Standards Institute (ANSI) C standard, as shown:</span></span>

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    <span data-ttu-id="8dfe8-121">Poiché MOF è basato su Unicode, è anche possibile specificare valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-121">Because MOF is based on Unicode, you can also specify 16-bit values.</span></span>

    <span data-ttu-id="8dfe8-122">Tenere presente che le costanti a carattere singolo nel formato ANSI C sono racchiuse tra virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-122">Be aware that single-character constants in ANSI C format are surrounded by double quotes.</span></span>

-   <span data-ttu-id="8dfe8-123">Racchiudere le stringhe di caratteri con virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-123">Surround character strings with double quotes.</span></span>

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   <span data-ttu-id="8dfe8-124">Concatena le stringhe di virgolette successive con uno o più spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-124">Concatenate successive quote strings with one or more white spaces.</span></span>

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   <span data-ttu-id="8dfe8-125">Usare una sequenza di escape che inizia con una barra rovesciata per incorporare le virgolette in una stringa.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-125">Use an escape sequence beginning with a backslash to embed quotes into a string.</span></span>

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

<span data-ttu-id="8dfe8-126">Nell'esempio seguente viene descritto come inizializzare le proprietà di stringa e un parametro di stringa:</span><span class="sxs-lookup"><span data-stu-id="8dfe8-126">The following example describes how to initialize string properties and a string parameter:</span></span>

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




