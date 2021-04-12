---
title: pipe (attributo)
description: Il costruttore del tipo di pipe consente di trasmettere un flusso aperto di dati tipizzati in una chiamata di procedura remota.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- attributo pipe MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336975"
---
# <a name="pipe-attribute"></a><span data-ttu-id="aa8fd-104">pipe (attributo)</span><span class="sxs-lookup"><span data-stu-id="aa8fd-104">pipe attribute</span></span>

<span data-ttu-id="aa8fd-105">Il costruttore del tipo di **pipe** consente di trasmettere un flusso aperto di dati tipizzati in una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-105">The **pipe** type constructor makes it possible to transmit an open-ended stream of typed data across a remote procedure call.</span></span>

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a><span data-ttu-id="aa8fd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa8fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa8fd-107">*tipo di elemento*</span><span class="sxs-lookup"><span data-stu-id="aa8fd-107">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="aa8fd-108">Definisce la dimensione di un singolo elemento nel buffer di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-108">Defines the size of a single element in the transfer buffer.</span></span> <span data-ttu-id="aa8fd-109">Il *tipo di elemento* può essere un [tipo di base](midl-base-types.md), un \_ tipo predefinito, uno [**struct**](struct.md), un' [**enumerazione 32B**](v1-enum.md)o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-109">The *element-type* can be a [base type](midl-base-types.md), predefined\_type, [**struct**](struct.md), [**32b enum**](v1-enum.md), or type identifier.</span></span> <span data-ttu-id="aa8fd-110">Diverse restrizioni si applicano ai *\_ tipi di elemento*, come descritto nella sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-110">Several restrictions apply to *element\_types*, as described in Remarks, below.</span></span>

</dd> <dt>

<span data-ttu-id="aa8fd-111">*pipe-dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="aa8fd-111">*pipe-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="aa8fd-112">Specifica uno o più identificatori o puntatori agli identificatori.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-112">Specifies one or more identifiers or pointers to identifiers.</span></span> <span data-ttu-id="aa8fd-113">Separare più dichiaratori con virgole.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-113">Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa8fd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa8fd-114">Remarks</span></span>

<span data-ttu-id="aa8fd-115">È possibile usare il costruttore del tipo di **pipe** per trasmettere i dati in entrambe le direzioni.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-115">You can use the **pipe** type constructor to transmit data in both directions.</span></span> <span data-ttu-id="aa8fd-116">Un **\[** [](in.md) **\]** parametro in pipe consente al server di eseguire il pull del flusso di dati dal client durante una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-116">An **\[**[**in**](in.md)**\]** pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="aa8fd-117">Un **\[** parametro [**out**](out-idl.md) **\]** pipe consente al server di eseguire il push del flusso di dati al client.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-117">An **\[**[**out**](out-idl.md)**\]** pipe parameter allows the server to push the data stream back to the client.</span></span> <span data-ttu-id="aa8fd-118">Le routine lato client vengono fornite per eseguire il push e il pull del flusso di dati e per allocare un buffer globale per i dati.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-118">You supply the client-side routines to push and pull the data stream and to allocate a global buffer for the data.</span></span> <span data-ttu-id="aa8fd-119">Le routine stub client e server eseguono il marshalling e l'unmarshalling dei dati e passano di nuovo un riferimento al buffer all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-119">The client and server stub routines marshal and unmarshal data and pass a reference to the buffer back to the application.</span></span>

<span data-ttu-id="aa8fd-120">Alle pipe si applicano le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa8fd-120">The following restrictions apply to pipes:</span></span>

-   <span data-ttu-id="aa8fd-121">Un elemento pipe non può essere o contenere un puntatore, una matrice conforme o variabile, un handle o un handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-121">A pipe element cannot be or contain a pointer, a conformant or varying array, a handle, or a context handle.</span></span> <span data-ttu-id="aa8fd-122">Inoltre, nell'implementazione Microsoft delle pipe, un elemento pipe non può essere o contenere un' [**Unione**](union.md), un' [**enumerazione 16B**](enum.md)o un [**\_ \_ int3264**](--int3264.md).</span><span class="sxs-lookup"><span data-stu-id="aa8fd-122">Also, in the Microsoft implementation of pipes, a pipe element cannot be or contain a [**union**](union.md), a [**16b enum**](enum.md), or an [**\_\_int3264**](--int3264.md).</span></span>
-   <span data-ttu-id="aa8fd-123">Non è possibile applicare gli **\[** attributi [**trasmissione \_ As**](transmit-as.md) **\]** , **\[** [**rappresenta \_ come**](represent-as.md) **\]** , **\[** [**\_ marshalling**](wire-marshal.md) **\]** o **\[** [**\_ marshalling utente**](user-marshal.md) **\]** a un tipo di pipe o al *tipo di elemento*.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-123">You cannot apply the **\[**[**transmit\_as**](transmit-as.md)**\]**, **\[**[**represent\_as**](represent-as.md)**\]**, **\[**[**wire\_marshal**](wire-marshal.md)**\]**, or **\[**[**user\_marshal**](user-marshal.md)**\]** attributes to a pipe type or to the *element-type*.</span></span>
-   <span data-ttu-id="aa8fd-124">Un tipo di pipe non può essere un membro di una struttura o di un'Unione, la destinazione di un puntatore o il tipo di base di una matrice.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-124">A pipe type cannot be a member of a structure or union, the target of a pointer, or the base type of an array.</span></span>
-   <span data-ttu-id="aa8fd-125">Un tipo di dati dichiarato come un tipo di pipe può essere utilizzato solo come parametro di una chiamata remota.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-125">A data type declared to be a pipe type can only be used as a parameter of a remote call.</span></span>
-   <span data-ttu-id="aa8fd-126">È possibile passare un parametro pipe in entrambe le direzioni per valore o per riferimento ( **\[** puntatore [**ref**](ref.md) **\]** ).</span><span class="sxs-lookup"><span data-stu-id="aa8fd-126">You can pass a pipe parameter in either direction by value or by reference (**\[**[**ref**](ref.md)**\]** pointer).</span></span> <span data-ttu-id="aa8fd-127">Tuttavia, non è possibile applicare l' **\[** [](ptr.md) **\]** attributo ptr a una pipe passata per riferimento.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-127">However you cannot apply the **\[**[**ptr**](ptr.md)**\]** attribute to a pipe that is passed by reference.</span></span> <span data-ttu-id="aa8fd-128">Non è possibile specificare un parametro pipe con un **\[** [](unique.md) **\]** puntatore univoco o completo, indipendentemente dalla direzione.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-128">You cannot specify a pipe parameter with a **\[**[**unique**](unique.md)**\]** or a full pointer, regardless of direction.</span></span>
-   <span data-ttu-id="aa8fd-129">Non è possibile utilizzare pipe nelle interfacce di **\[** [**oggetti**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="aa8fd-129">You cannot use pipes in **\[**[**object**](object.md)**\]** interfaces.</span></span>
-   <span data-ttu-id="aa8fd-130">Non è possibile applicare l' **\[** [](idempotent.md) **\]** attributo idempotente a una routine con un parametro pipe.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-130">You cannot apply the **\[**[**idempotent**](idempotent.md)**\]** attribute to a routine that has a pipe parameter.</span></span>
-   <span data-ttu-id="aa8fd-131">Non è possibile usare gli attributi di serializzazione, **\[** [**codificare**](encode.md) **\]** e **\[** [**decodificare**](decode.md) **\]** con pipe.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-131">You cannot use the serialization attributes, **\[**[**encode**](encode.md)**\]** and **\[**[**decode**](decode.md)**\]** with pipes.</span></span>
-   <span data-ttu-id="aa8fd-132">Non è possibile usare handle automatici, per impostazione predefinita o con l' **\[** [**attributo \_ handle automatico**](auto-handle.md) **\]** , con pipe.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-132">You cannot use automatic handles, either by default, or with the **\[**[**auto\_handle**](auto-handle.md)**\]** attribute, with pipes.</span></span>

> [!Note]  
> <span data-ttu-id="aa8fd-133">Il compilatore MIDL supporta solo le pipe in modalità [**/OIF**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="aa8fd-133">The MIDL compiler supports pipes in [**/Oif**](-oi.md) mode only.</span></span>

 

<span data-ttu-id="aa8fd-134">Per ulteriori informazioni sull'implementazione di routine con i parametri pipe, vedere [Pipes](/windows/desktop/Rpc/pipes) in the RPC Programmer ' s Guide and Reference.</span><span class="sxs-lookup"><span data-stu-id="aa8fd-134">For more information on implementing routines with pipe parameters, see [Pipes](/windows/desktop/Rpc/pipes) in the RPC Programmer's Guide and Reference.</span></span>

## <a name="examples"></a><span data-ttu-id="aa8fd-135">Esempi</span><span class="sxs-lookup"><span data-stu-id="aa8fd-135">Examples</span></span>

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a><span data-ttu-id="aa8fd-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="aa8fd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa8fd-137">**\_handle automatico**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-137">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-138">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="aa8fd-138">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-139">**decodificare**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-139">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-140">**codificare**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-140">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-141">**enum**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-141">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-142">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-142">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-143">**in**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-143">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-144">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-144">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-145">**out**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-146">**ptr**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-146">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-147">**ref**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-147">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-148">**rappresenta \_ come**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-148">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-149">**struct**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-149">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-150">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-150">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-151">**unico**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-151">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-152">**\_marshalling utente**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-152">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="aa8fd-153">**\_marshalling di rete**</span><span class="sxs-lookup"><span data-stu-id="aa8fd-153">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> </dl>

 

 