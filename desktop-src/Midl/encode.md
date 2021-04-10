---
title: codifica attributo
description: L'attributo \ Encode \ ACF specifica che una routine o un tipo di dati necessita del supporto della serializzazione.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- codifica attributo MIDL
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956377"
---
# <a name="encode-attribute"></a><span data-ttu-id="71f05-104">codifica attributo</span><span class="sxs-lookup"><span data-stu-id="71f05-104">encode attribute</span></span>

<span data-ttu-id="71f05-105">L'attributo **\[ Encode \]** ACF specifica che una routine o un tipo di dati necessita del supporto della serializzazione.</span><span class="sxs-lookup"><span data-stu-id="71f05-105">The **\[encode\]** ACF attribute specifies that a procedure or a data type needs serialization support.</span></span>

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a><span data-ttu-id="71f05-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="71f05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f05-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="71f05-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="71f05-108">Specifica altri attributi che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="71f05-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="71f05-109">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="71f05-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="71f05-110">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="71f05-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="71f05-111">*interfaccia-definizione*</span><span class="sxs-lookup"><span data-stu-id="71f05-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="71f05-112">Specifica le istruzioni IDL che formano la definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="71f05-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="71f05-113">*op-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="71f05-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="71f05-114">Specifica altri attributi operativi che si applicano alla procedura, ad esempio **\[** [**Decode**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="71f05-114">Specifies other operational attributes that apply to the procedure such as **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="71f05-115">*proc-name*</span><span class="sxs-lookup"><span data-stu-id="71f05-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="71f05-116">Specifica il nome della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="71f05-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="71f05-117">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="71f05-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="71f05-118">Specifica altri attributi applicabili al tipo, ad esempio **\[** [**Decode**](decode.md) **\]** e **\[** [**allocate**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="71f05-118">Specifies other attributes that apply to the type such as **\[**[**decode**](decode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="71f05-119">*Nome-tipo*</span><span class="sxs-lookup"><span data-stu-id="71f05-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="71f05-120">Specifica un tipo definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="71f05-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71f05-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="71f05-121">Remarks</span></span>

<span data-ttu-id="71f05-122">L'attributo **\[ Encode \]** induce il compilatore MIDL a generare codice che un'applicazione può usare per serializzare i dati in un buffer.</span><span class="sxs-lookup"><span data-stu-id="71f05-122">The **\[encode\]** attribute causes the MIDL compiler to generate code that an application can use to serialize data into a buffer.</span></span> <span data-ttu-id="71f05-123">L' **\[** [](decode.md) **\]** attributo Decode genera il codice per l'unmarshalling dei dati da un buffer.</span><span class="sxs-lookup"><span data-stu-id="71f05-123">The **\[**[**decode**](decode.md)**\]** attribute generates the code for unmarshaling data from a buffer.</span></span>

<span data-ttu-id="71f05-124">Utilizzare gli attributi **\[ Encode \]** e **\[** [**Decode**](decode.md) **\]** in un oggetto ACF per generare il codice di serializzazione per le procedure o i tipi definiti nel file IDL di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="71f05-124">Use the **\[encode\]** and **\[**[**decode**](decode.md)**\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="71f05-125">Quando viene utilizzato come attributo di interfaccia, la **\[ codifica \]** viene applicata a tutti i tipi e le procedure definiti nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="71f05-125">When used as an interface attribute, **\[encode\]** applies to all the types and procedures defined in the IDL file.</span></span> <span data-ttu-id="71f05-126">Quando viene usato come attributo operativo, la **\[ codifica \]** viene applicata solo alla procedura specificata.</span><span class="sxs-lookup"><span data-stu-id="71f05-126">When used as an operational attribute, **\[encode\]** applies only to the specified procedure.</span></span> <span data-ttu-id="71f05-127">Quando viene usato come attributo di tipo, **\[ Encode \]** si applica solo al tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="71f05-127">When used as a type attribute, **\[encode\]** applies only to the specified type.</span></span>

<span data-ttu-id="71f05-128">Quando si applica l'attributo **\[ Encode \]** o **\[** [**Decode**](decode.md) **\]** a una routine, il compilatore MIDL genera uno stub di serializzazione in modo simile, perché vengono generati stub remoti per routine remote.</span><span class="sxs-lookup"><span data-stu-id="71f05-128">When the **\[encode\]** or **\[**[**decode**](decode.md)**\]** attribute is applied to a procedure, the MIDL compiler generates a serialization stub in a similar fashion as remote stubs are generated for remote routines.</span></span> <span data-ttu-id="71f05-129">Una routine può essere una procedura remota o di serializzazione, ma non può essere entrambe.</span><span class="sxs-lookup"><span data-stu-id="71f05-129">A procedure can be either a remote or a serializing procedure, but it cannot be both.</span></span> <span data-ttu-id="71f05-130">Il prototipo della routine generata viene inviato allo STUB. File H quando lo stub entra nel \_ file c. c dello stub.</span><span class="sxs-lookup"><span data-stu-id="71f05-130">The prototype of the generated routine is sent to the STUB.H file while the stub itself goes into the STUB\_C.C file.</span></span>

<span data-ttu-id="71f05-131">Il compilatore MIDL genera due funzioni per ogni tipo a cui viene applicato l'attributo **\[ \] Encode** e una funzione aggiuntiva per ogni tipo **\[** [](decode.md) **\]** a cui viene applicato l'attributo Decode.</span><span class="sxs-lookup"><span data-stu-id="71f05-131">The MIDL compiler generates two functions for each type the **\[encode\]** attribute applies to, and one additional function for each type the **\[**[**decode**](decode.md)**\]** attribute applies to.</span></span> <span data-ttu-id="71f05-132">Ad esempio, per un tipo definito dall'utente denominato MyType, il compilatore genera il codice per le \_ funzioni MyType Encode, MyType \_ Decode e MyType \_ AlignSize.</span><span class="sxs-lookup"><span data-stu-id="71f05-132">For example, for a user-defined type named MyType, the compiler generates code for the MyType\_Encode, MyType\_Decode, and MyType\_AlignSize functions.</span></span> <span data-ttu-id="71f05-133">Per queste funzioni, il compilatore scrive i prototipi nello STUB. H e codice sorgente per STUB \_ C.C.</span><span class="sxs-lookup"><span data-stu-id="71f05-133">For these functions, the compiler writes prototypes to STUB.H and source code to STUB\_C.C.</span></span>

<span data-ttu-id="71f05-134">Per ulteriori informazioni sugli handle di serializzazione e sulla codifica o la decodifica dei dati, vedere [servizi di serializzazione](/windows/desktop/Rpc/serialization-services).</span><span class="sxs-lookup"><span data-stu-id="71f05-134">For additional information about serialization handles and encoding or decoding data, see [Serialization Services](/windows/desktop/Rpc/serialization-services).</span></span>

## <a name="examples"></a><span data-ttu-id="71f05-135">Esempi</span><span class="sxs-lookup"><span data-stu-id="71f05-135">Examples</span></span>

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a><span data-ttu-id="71f05-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="71f05-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f05-137">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="71f05-137">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="71f05-138">**allocare**</span><span class="sxs-lookup"><span data-stu-id="71f05-138">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="71f05-139">**decodificare**</span><span class="sxs-lookup"><span data-stu-id="71f05-139">**decode**</span></span>](decode.md)
</dt> </dl>

 

 