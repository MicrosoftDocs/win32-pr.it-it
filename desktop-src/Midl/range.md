---
title: range (attributo)
description: L'attributo \ range \ consente di specificare un intervallo di valori consentiti per argomenti o campi i cui valori sono impostati in fase di esecuzione. Quando viene usato con un tipo di pipe, l'attributo specifica l'intervallo consentito per il numero di elementi nei blocchi di pipe.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- attributo di intervallo MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299633"
---
# <a name="range-attribute"></a><span data-ttu-id="46456-105">range (attributo)</span><span class="sxs-lookup"><span data-stu-id="46456-105">range attribute</span></span>

<span data-ttu-id="46456-106">L'attributo **\[ Range \]** consente di specificare un intervallo di valori consentiti per gli argomenti o i campi i cui valori vengono impostati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="46456-106">The **\[range\]** attribute lets you specify a range of allowable values for arguments or fields whose values are set at run time.</span></span> <span data-ttu-id="46456-107">Quando viene usato con un tipo di pipe, l'attributo specifica l'intervallo consentito per il numero di elementi nei blocchi di pipe.</span><span class="sxs-lookup"><span data-stu-id="46456-107">When used with a pipe type, the attribute specifies the allowable range for the count of elements in the pipe chunks.</span></span>

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a><span data-ttu-id="46456-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46456-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46456-109">*bassa Val*</span><span class="sxs-lookup"><span data-stu-id="46456-109">*low-val*</span></span> 
</dt> <dd>

<span data-ttu-id="46456-110">Valore minimo consentito che il parametro o il campo può tenere.</span><span class="sxs-lookup"><span data-stu-id="46456-110">The lowest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="46456-111">*alta Val*</span><span class="sxs-lookup"><span data-stu-id="46456-111">*high-val*</span></span> 
</dt> <dd>

<span data-ttu-id="46456-112">Valore massimo consentito che il parametro o il campo può tenere.</span><span class="sxs-lookup"><span data-stu-id="46456-112">The highest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="46456-113">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="46456-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="46456-114">Un tipo integrale diverso da [**Hyper**](hyper.md) o [**\_ \_ Int64**](--int64.md), un identificatore di tipo a un tipo integrale, un tipo [**enum**](enum.md) o un nome di tipo di pipe.</span><span class="sxs-lookup"><span data-stu-id="46456-114">An integral type other than [**hyper**](hyper.md) or [**\_\_int64**](--int64.md), a type identifier to an integral type, an [**enum**](enum.md) type, or a pipe type name.</span></span>

</dd> <dt>

<span data-ttu-id="46456-115">*dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="46456-115">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="46456-116">Dichiaratore C standard, ad esempio un identificatore.</span><span class="sxs-lookup"><span data-stu-id="46456-116">A standard C declarator, such as an identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46456-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="46456-117">Remarks</span></span>

<span data-ttu-id="46456-118">Usare l'attributo **\[ Range \]** per modificare il significato dei parametri sensibili o dei campi, ad esempio quelli usati per le dimensioni o la lunghezza, con matrici conformi o variabili; oppure ogni volta che si vuole controllare un parametro o un valore di campo rispetto a un intervallo di valori validi.</span><span class="sxs-lookup"><span data-stu-id="46456-118">Use the **\[range\]** attribute to modify the meaning of sensitive parameters or fields, such as those used for size or length, with conformant or varying arrays; or whenever you want to check a parameter or field value against a range of valid values.</span></span> <span data-ttu-id="46456-119">L'attributo è applicabile ai parametri di primo livello, oltre ai parametri e ai campi di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="46456-119">The attribute is applicable to top-level parameters as well as lower-level parameters and fields.</span></span> <span data-ttu-id="46456-120">L'aggiunta dell'attributo di **\[ intervallo \]** a un tipo non comporta la modifica del formato wire, quindi non influisce sulla compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="46456-120">Adding the **\[range\]** attribute to a type does not change its wire format, thus does not affect backward compatibility.</span></span>

<span data-ttu-id="46456-121">L'attributo **\[ Range \]** può essere usato anche su dati conformi, ad esempio buffer o matrici con un attributo di conformità.</span><span class="sxs-lookup"><span data-stu-id="46456-121">The **\[range\]** attribute can also be used on conformant data such as buffers or arrays with a conformance attribute.</span></span> <span data-ttu-id="46456-122">L'effetto è quello di limitare tutte le dimensioni di conformità per i dati conformi all'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="46456-122">The effect is to limit all conformance sizes for the conformant data to the specified range.</span></span> <span data-ttu-id="46456-123">Se i dati conformi sono matrici multidimensionali, ogni dimensione della matrice è limitata all'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="46456-123">If the conformant data is a multi-dimensional array, each array dimension is limited to the specified range.</span></span>

<span data-ttu-id="46456-124">Per usare l' **\[ intervallo \]** nei dati conformi, è necessario che la destinazione della compilazione sia "$" di destinazione nt60 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="46456-124">Use of **\[range\]** on conformant data requires that the compilation target be â€“target NT60 or higher.</span></span>

<span data-ttu-id="46456-125">Si noti che è necessario usare l'opzione del compilatore [**/robust**](-robust.md) quando si compila il file IDL per generare il codice stub che eseguirà questi controlli.</span><span class="sxs-lookup"><span data-stu-id="46456-125">Note that you must use the [**/robust**](-robust.md) compiler option when you compile your IDL file in order to generate the stub code that will perform these checks.</span></span> <span data-ttu-id="46456-126">Senza l'opzione **/robust** , il compilatore MIDL ignora questo attributo.</span><span class="sxs-lookup"><span data-stu-id="46456-126">Without the **/robust** switch, the MIDL compiler ignores this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="46456-127">Esempi</span><span class="sxs-lookup"><span data-stu-id="46456-127">Examples</span></span>

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a><span data-ttu-id="46456-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="46456-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46456-129">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="46456-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="46456-130">matrici</span><span class="sxs-lookup"><span data-stu-id="46456-130">arrays</span></span>](/windows/desktop/Rpc/arrays)
</dt> <dt>

[<span data-ttu-id="46456-131">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="46456-131">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="46456-132">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="46456-132">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="46456-133">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="46456-133">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="46456-134">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="46456-134">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="46456-135">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="46456-135">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="46456-136">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="46456-136">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="46456-137">**opzione \_**</span><span class="sxs-lookup"><span data-stu-id="46456-137">**switch\_is**</span></span>](switch-is.md)
</dt> </dl>

 

 