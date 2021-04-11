---
title: Risorsa User-Defined
description: Un'istruzione di definizione delle risorse definita dall'utente definisce una risorsa che contiene dati specifici dell'applicazione.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- risorsa definita dall'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221364"
---
# <a name="user-defined-resource"></a><span data-ttu-id="21b1c-104">Risorsa User-Defined</span><span class="sxs-lookup"><span data-stu-id="21b1c-104">User-Defined Resource</span></span>

<span data-ttu-id="21b1c-105">Un'istruzione di definizione delle risorse definita dall'utente definisce una risorsa che contiene dati specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21b1c-105">A user-defined resource-definition statement defines a resource that contains application-specific data.</span></span> <span data-ttu-id="21b1c-106">I dati possono avere qualsiasi formato e possono essere definiti come contenuto di un determinato file (se il parametro *filename* viene specificato) o come una serie di numeri e stringhe (se il blocco di *dati non elaborati* è specificato).</span><span class="sxs-lookup"><span data-stu-id="21b1c-106">The data can have any format and can be defined either as the content of a given file (if the *filename* parameter is given) or as a series of numbers and strings (if the *raw-data* block is specified).</span></span>

``` syntax
nameID typeID filename
```

<span data-ttu-id="21b1c-107">*Filename* specifica il nome di un file contenente i dati binari della risorsa.</span><span class="sxs-lookup"><span data-stu-id="21b1c-107">The *filename* specifies the name of a file containing the binary data of the resource.</span></span> <span data-ttu-id="21b1c-108">Il contenuto del file è incluso come risorsa.</span><span class="sxs-lookup"><span data-stu-id="21b1c-108">The contents of the file are included as the resource.</span></span> <span data-ttu-id="21b1c-109">RC non interpreta i dati binari in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="21b1c-109">RC does not interpret the binary data in any way.</span></span> <span data-ttu-id="21b1c-110">È responsabilità del programmatore garantire che i dati siano allineati correttamente per l'architettura del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="21b1c-110">It is the programmer's responsibility to ensure that the data is properly aligned for the target computer architecture.</span></span>

<span data-ttu-id="21b1c-111">È anche possibile definire completamente una risorsa definita dall'utente nello script della risorsa usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="21b1c-111">A user-defined resource can also be defined completely in the resource script using the following syntax:</span></span>

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a><span data-ttu-id="21b1c-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="21b1c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21b1c-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="21b1c-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="21b1c-114">Nome univoco o Unsigned Integer a 16 bit che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="21b1c-114">Unique name or a 16-bit unsigned integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="21b1c-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span><span class="sxs-lookup"><span data-stu-id="21b1c-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span></span>
</dt> <dd>

<span data-ttu-id="21b1c-116">Nome univoco o Unsigned Integer a 16 bit che identifica il tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="21b1c-116">Unique name or a 16-bit unsigned integer that identifies the resource type.</span></span> <span data-ttu-id="21b1c-117">Se viene specificato un numero, il valore deve essere maggiore di 255.</span><span class="sxs-lookup"><span data-stu-id="21b1c-117">If a number is given, it must be greater than 255.</span></span> <span data-ttu-id="21b1c-118">I numeri da 1 a 255 sono riservati ai tipi di risorse ridefiniti esistenti e futuri.</span><span class="sxs-lookup"><span data-stu-id="21b1c-118">The numbers 1 through 255 are reserved for existing and future redefined resource types.</span></span>

</dd> <dt>

<span data-ttu-id="21b1c-119"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="21b1c-119"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="21b1c-120">Nome del file che contiene i dati della risorsa.</span><span class="sxs-lookup"><span data-stu-id="21b1c-120">Name of the file that contains the resource data.</span></span> <span data-ttu-id="21b1c-121">Il parametro deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="21b1c-121">The parameter must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span>

</dd> <dt>

<span data-ttu-id="21b1c-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*dati non elaborati*</span><span class="sxs-lookup"><span data-stu-id="21b1c-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="21b1c-123">Dati non elaborati costituiti da uno o più numeri interi o stringhe di caratteri.</span><span class="sxs-lookup"><span data-stu-id="21b1c-123">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="21b1c-124">I numeri interi possono essere specificati in formato decimale, ottale o esadecimale.</span><span class="sxs-lookup"><span data-stu-id="21b1c-124">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="21b1c-125">Per essere compatibile con Windows a 16 bit, i numeri interi vengono archiviati come valori di WORD.</span><span class="sxs-lookup"><span data-stu-id="21b1c-125">To be compatible with 16-bit Windows, integers are stored as WORD values.</span></span> <span data-ttu-id="21b1c-126">È possibile archiviare un valore integer come valore DWORD qualificando l'Integer con il suffisso "L".</span><span class="sxs-lookup"><span data-stu-id="21b1c-126">You can store an integer as a DWORD value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="21b1c-127">Le stringhe sono racchiuse tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="21b1c-127">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="21b1c-128">RC non aggiunge automaticamente un carattere di terminazione null a una stringa.</span><span class="sxs-lookup"><span data-stu-id="21b1c-128">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="21b1c-129">Ogni stringa è una sequenza dei caratteri ANSI specificati, a meno che non venga qualificata come stringa di caratteri wide con il prefisso "L".</span><span class="sxs-lookup"><span data-stu-id="21b1c-129">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the "L" prefix.</span></span>

<span data-ttu-id="21b1c-130">Il blocco di dati inizia in un limite **DWORD** e RC non esegue la spaziatura interna o l'allineamento dei dati all'interno del blocco di *dati non elaborati* .</span><span class="sxs-lookup"><span data-stu-id="21b1c-130">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="21b1c-131">È responsabilità del programmatore garantire l'allineamento corretto dei dati all'interno del blocco.</span><span class="sxs-lookup"><span data-stu-id="21b1c-131">It is the programmer's responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="21b1c-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="21b1c-132">Example</span></span>

<span data-ttu-id="21b1c-133">Nell'esempio seguente vengono illustrate diverse istruzioni definite dall'utente:</span><span class="sxs-lookup"><span data-stu-id="21b1c-133">The following example shows several user-defined statements:</span></span>

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




