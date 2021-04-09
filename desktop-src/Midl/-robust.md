---
title: opzione/robust
description: L'opzione/robust indica al compilatore MIDL di generare ulteriori informazioni sul controllo degli errori, utilizzate dal motore di recapito dell'integrità per eseguire controlli di integrità in fase di esecuzione.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- /Robust switch MIDL
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857238"
---
# <a name="robust-switch"></a><span data-ttu-id="873f5-104">opzione/robust</span><span class="sxs-lookup"><span data-stu-id="873f5-104">/robust switch</span></span>

<span data-ttu-id="873f5-105">L'opzione **/robust** indica al compilatore MIDL di generare ulteriori informazioni sul controllo degli errori, utilizzate dal motore di recapito dell'integrità per eseguire controlli di integrità in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="873f5-105">The **/robust** switch tells the MIDL compiler to generate additional error-checking information, which the NDR engine uses to perform integrity checks at run time.</span></span>

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a><span data-ttu-id="873f5-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="873f5-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="873f5-107">*/Oicf*</span><span class="sxs-lookup"><span data-stu-id="873f5-107">*/Oicf*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="873f5-108">*/OIF*</span><span class="sxs-lookup"><span data-stu-id="873f5-108">*/Oif*</span></span> 
</dt> <dd>

<span data-ttu-id="873f5-109">Queste opzioni sono identiche nelle rispettive funzionalità.</span><span class="sxs-lookup"><span data-stu-id="873f5-109">These switches are identical in their functionality.</span></span> <span data-ttu-id="873f5-110">Specificano il metodo proxy codificato per il marshalling e utilizzano stringhe di formato rapido per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="873f5-110">They specify the codeless proxy method of marshaling and use fast format strings for improved performance.</span></span> <span data-ttu-id="873f5-111">Vedere/ [**OI**](-oi.md).</span><span class="sxs-lookup"><span data-stu-id="873f5-111">See / [**Oi**](-oi.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="873f5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="873f5-112">Remarks</span></span>

<span data-ttu-id="873f5-113">L'utilizzo dell'opzione **/robust** genera informazioni aggiuntive che consentono al motore di rappresentazione dei dati di rete (NDR) di eseguire il controllo degli errori di run-time sugli argomenti correlati in matrici dinamiche, unioni e puntatori di interfaccia in [**uscita**](out-idl.md) nelle applicazioni DCOM.</span><span class="sxs-lookup"><span data-stu-id="873f5-113">Using the **/robust** switch generates additional information that allows the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in [**out**](out-idl.md) interface pointers in DCOM applications.</span></span> <span data-ttu-id="873f5-114">L'opzione **/robust** è disponibile solo in Windows 2000 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="873f5-114">The **/robust** switch is only available under WindowsÂ 2000 and later versions of Windows.</span></span>

<span data-ttu-id="873f5-115">Un argomento correlato è un argomento che usa uno degli attributi che consentono di determinare la dimensione di un oggetto dati in fase di esecuzione: [**size \_ è**](size-is.md), [**length \_ è**](length-is.md), [**First \_ è**](first-is.md), [**Last \_ is**](last-is.md), [**Max \_ is**](max-is.md), [**Switch \_ is**](switch-is.md)e [**IID \_ è**](iid-is.md).</span><span class="sxs-lookup"><span data-stu-id="873f5-115">A correlated argument is an argument that uses any of the attributes that allow the size of a data object to be determined at run time: [**size\_is**](size-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**max\_is**](max-is.md), [**switch\_is**](switch-is.md), and [**iid\_is**](iid-is.md).</span></span> <span data-ttu-id="873f5-116">In conformità con la specifica OSF-DCE per la rappresentazione Wire, questo argomento correlato viene visualizzato in due posizioni diverse.</span><span class="sxs-lookup"><span data-stu-id="873f5-116">In accordance with the OSF-DCE specification for the wire representation, this correlated argument appears in two different places.</span></span> <span data-ttu-id="873f5-117">Si consideri, ad esempio, un utilizzo tipico della **dimensione \_ è** attribute:</span><span class="sxs-lookup"><span data-stu-id="873f5-117">For example, consider a typical usage of the **size\_is** attribute:</span></span>

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

<span data-ttu-id="873f5-118">In questo esempio, il client passa un valore Long che specifica la dimensione di un blocco di \_ tipi di barre (in termini di numero di elementi dei tipi di barre \_ ) e un puntatore al blocco effettivo dei tipi di barre \_ .</span><span class="sxs-lookup"><span data-stu-id="873f5-118">In this example, the client passes a long that specifies the size of a block of BAR\_TYPEs (in terms of number of BAR\_TYPES elements), and a pointer to the actual block of BAR\_TYPEs.</span></span> <span data-ttu-id="873f5-119">L'argomento size è correlato all'argomento pBarType.</span><span class="sxs-lookup"><span data-stu-id="873f5-119">The Size argument correlates with the pBarType argument.</span></span> <span data-ttu-id="873f5-120">In conformità con la specifica OSF-DCE, l'argomento di dimensione viene rappresentato due volte in rete, prima come se stesso e quindi con la matrice di \_ elementi di tipo barra che rappresentano l'argomento pBarType.</span><span class="sxs-lookup"><span data-stu-id="873f5-120">In accordance with the OSF-DCE specification, the Size argument is represented twice on the wire—first as itself and then with the array of BAR\_TYPE elements that represent the pBarType argument.</span></span> <span data-ttu-id="873f5-121">Ogni argomento viene sottoposto a unmarshalling indipendentemente, in base alla propria rappresentazione in transito.</span><span class="sxs-lookup"><span data-stu-id="873f5-121">Each argument is unmarshaled independently, according to its own wire representation.</span></span> <span data-ttu-id="873f5-122">In genere, l'argomento size e la relativa copia, usato per rappresentare parte dell'altro argomento, hanno gli stessi valori.</span><span class="sxs-lookup"><span data-stu-id="873f5-122">Normally, the Size argument and its copy, which is used to represent part of the other argument, have the same values.</span></span> <span data-ttu-id="873f5-123">Tuttavia, se l'argomento di dimensione viene danneggiato, ad esempio quando il blocco di tipi di barre \_ è maggiore di quello allocato, l'applicazione server potrebbe non rispondere, perché usa il valore dell'argomento size per misurare i dati in ingresso.</span><span class="sxs-lookup"><span data-stu-id="873f5-123">However, if the Size argument becomes corrupted (for example, when the block of BAR\_TYPES is larger than what was allocated), the server application may stop responding, because it uses the value of the Size argument to measure incoming data.</span></span>

<span data-ttu-id="873f5-124">L'opzione **/robust** è necessaria per implementare il controllo dell'intervallo valido con l'attributo [**Range**](range.md) .</span><span class="sxs-lookup"><span data-stu-id="873f5-124">The **/robust** switch is required to implement valid range checking with the [**range**](range.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="873f5-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="873f5-125">Examples</span></span>

<span data-ttu-id="873f5-126">**MIDL/robust/Oicf nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="873f5-126">**midl /robust /Oicf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="873f5-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="873f5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873f5-128">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="873f5-128">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="873f5-129">**/OI**</span><span class="sxs-lookup"><span data-stu-id="873f5-129">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="873f5-130">**intervallo**</span><span class="sxs-lookup"><span data-stu-id="873f5-130">**range**</span></span>](range.md)
</dt> </dl>

 

 




