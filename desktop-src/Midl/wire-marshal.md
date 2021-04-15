---
title: wire_marshal (attributo)
description: L'attributo \ Wire \_ Marshal \ specifica un tipo di dati che verrà usato per la trasmissione (il tipo Wire) invece di un tipo di dati specifico dell'applicazione (User-Type).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- attributo wire_marshal MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399851"
---
# <a name="wire_marshal-attribute"></a><span data-ttu-id="1807b-104">\_attributo Wire Marshal</span><span class="sxs-lookup"><span data-stu-id="1807b-104">wire\_marshal attribute</span></span>

<span data-ttu-id="1807b-105">L'attributo **\[ Wire \_ Marshal \]** specifica un tipo di dati che verrà usato per la trasmissione (il *tipo Wire*) invece di un tipo di dati specifico dell'applicazione ( *User-Type*).</span><span class="sxs-lookup"><span data-stu-id="1807b-105">The **\[wire\_marshal\]** attribute specifies a data type that will be used for transmission (the *wire-type*) instead of an application-specific data type (the *userm-type*).</span></span>

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="1807b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1807b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1807b-107">*tipo Wire*</span><span class="sxs-lookup"><span data-stu-id="1807b-107">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1807b-108">Specifica il tipo di dati di trasferimento denominato effettivamente trasferito tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="1807b-108">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="1807b-109">Il *tipo di collegamento* deve essere un tipo di base MIDL, un tipo predefinito o un identificatore di tipo di un tipo che può essere trasmesso attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="1807b-109">The *wire-type* must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="1807b-110">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="1807b-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="1807b-111">Tipo per il quale *UserY-Type* diventerà un alias.</span><span class="sxs-lookup"><span data-stu-id="1807b-111">The type for which *userm-type* will become an alias.</span></span>

</dd> <dt>

<span data-ttu-id="1807b-112">*utente-tipo*</span><span class="sxs-lookup"><span data-stu-id="1807b-112">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1807b-113">Specifica l'identificatore del tipo di dati utente di cui effettuare il marshalling.</span><span class="sxs-lookup"><span data-stu-id="1807b-113">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="1807b-114">Può trattarsi di qualsiasi tipo, come specificato da *Type-specifier*, purché disponga di una dimensione ben definita.</span><span class="sxs-lookup"><span data-stu-id="1807b-114">It can be any type, as given by the *type-specifier*, as long as it has a well-defined size.</span></span> <span data-ttu-id="1807b-115">Il *tipo di utente* non deve essere transmittable, ma deve essere un tipo noto al compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="1807b-115">The *userm-type* need not be transmittable but must be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="1807b-116">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="1807b-116">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="1807b-117">Specifica un puntatore a un campo del flag ( [**Long**](long.md) [**senza segno**](unsigned.md) ).</span><span class="sxs-lookup"><span data-stu-id="1807b-117">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="1807b-118">La parola più significativa specifica i flag di rappresentazione dei dati NDR come definito da DCE per la rappresentazione a virgola mobile, Big o little-endian e character.</span><span class="sxs-lookup"><span data-stu-id="1807b-118">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="1807b-119">La parola di ordine inferiore specifica un flag di contesto di marshalling.</span><span class="sxs-lookup"><span data-stu-id="1807b-119">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="1807b-120">Il layout esatto dei flag viene descritto nella [funzione di tipo \_ UserSize](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="1807b-120">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="1807b-121">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="1807b-121">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="1807b-122">Specifica la dimensione del buffer corrente (offset) prima di ridimensionare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1807b-122">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="1807b-123">*\_TypeObject Puser*</span><span class="sxs-lookup"><span data-stu-id="1807b-123">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="1807b-124">Specifica un puntatore a un oggetto di *tipo User \_ .*</span><span class="sxs-lookup"><span data-stu-id="1807b-124">Specifies a pointer to an object of *userm\_type.*</span></span>

</dd> <dt>

<span data-ttu-id="1807b-125">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="1807b-125">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="1807b-126">Specifica il puntatore al buffer corrente.</span><span class="sxs-lookup"><span data-stu-id="1807b-126">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1807b-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="1807b-127">Remarks</span></span>

<span data-ttu-id="1807b-128">Ogni tipo di dati specifico dell'applicazione, *User-Type,* presenta una corrispondenza uno-a-uno con un *tipo Wire* che definisce la rappresentazione in transito del tipo.</span><span class="sxs-lookup"><span data-stu-id="1807b-128">Each application-specific data type, *userm-type,* has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="1807b-129">È necessario specificare routine per dimensionare i dati per il marshalling, per effettuare il marshalling e l'unmarshalling dei dati e per liberare memoria.</span><span class="sxs-lookup"><span data-stu-id="1807b-129">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="1807b-130">Si noti che se nei dati sono presenti tipi incorporati anch ' essi definiti con **\[ \_ marshalling \] di rete** o **\[** [**\_ marshalling dell'utente**](user-marshal.md) **\]** , è necessario gestire anche la manutenzione di tali tipi incorporati.</span><span class="sxs-lookup"><span data-stu-id="1807b-130">Note that if there are embedded types in your data that are also defined with **\[wire\_marshal\]** or **\[**[**user\_marshal**](user-marshal.md)**\]**, you need to manage the servicing of those embedded types also.</span></span> <span data-ttu-id="1807b-131">Per ulteriori informazioni su queste routine, vedere [l'attributo Wire \_ Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="1807b-131">For more information on these routines, see [The wire\_marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute).</span></span>

<span data-ttu-id="1807b-132">L'implementazione deve seguire le regole di marshalling in base alla specifica OSF-DCE.</span><span class="sxs-lookup"><span data-stu-id="1807b-132">Your implementation must follow the marshalling rules according to the OSF-DCE specification.</span></span> <span data-ttu-id="1807b-133">Per informazioni dettagliate sulla sintassi di trasferimento del rapporto di recapito [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) , vedere.</span><span class="sxs-lookup"><span data-stu-id="1807b-133">Details about NDR transfer syntax can be found at [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).</span></span> <span data-ttu-id="1807b-134">Se non si ha familiarità con il protocollo wire, non è consigliabile usare il **\[ \_ marshalling \] di rete** .</span><span class="sxs-lookup"><span data-stu-id="1807b-134">It is not recommended to use **\[wire\_marshal\]** if you are not familiar with the wire protocol.</span></span>

<span data-ttu-id="1807b-135">Il *tipo di collegamento* non può essere un puntatore di interfaccia o un puntatore completo.</span><span class="sxs-lookup"><span data-stu-id="1807b-135">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="1807b-136">Il *tipo di Wire* deve avere una dimensione di memoria ben definita.</span><span class="sxs-lookup"><span data-stu-id="1807b-136">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="1807b-137">Per informazioni dettagliate su come effettuare il marshalling di un determinato *tipo di Wire*, vedere [regole di marshalling per \_ marshalling degli utenti e \_ marshalling di rete](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .</span><span class="sxs-lookup"><span data-stu-id="1807b-137">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="1807b-138">Il *tipo di utente* non deve essere un puntatore di interfaccia perché è possibile effettuare il marshalling direttamente.</span><span class="sxs-lookup"><span data-stu-id="1807b-138">The *userm-type* should not be an interface pointer because these can be marshaled directly.</span></span> <span data-ttu-id="1807b-139">Se il tipo di utente è un puntatore completo, è necessario gestire manualmente l'alias.</span><span class="sxs-lookup"><span data-stu-id="1807b-139">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

<span data-ttu-id="1807b-140">Non è possibile usare l'attributo **\[ Wire \_ Marshal \]** con l' **\[** attributo [**allocate**](allocate.md) **\]** , direttamente o indirettamente, perché il motore NDR non controlla l'allocazione di memoria per il tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="1807b-140">You cannot use the **\[wire\_marshal\]** attribute with the **\[**[**allocate**](allocate.md)**\]** attribute, either directly or indirectly, because the NDR engine does not control memory allocation for the transmitted type.</span></span>

## <a name="examples"></a><span data-ttu-id="1807b-141">Esempi</span><span class="sxs-lookup"><span data-stu-id="1807b-141">Examples</span></span>

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a><span data-ttu-id="1807b-142">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1807b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1807b-143">**allocare**</span><span class="sxs-lookup"><span data-stu-id="1807b-143">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="1807b-144">Rappresentazione dei dati</span><span class="sxs-lookup"><span data-stu-id="1807b-144">Data Representation</span></span>](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[<span data-ttu-id="1807b-145">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="1807b-145">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="1807b-146">**long**</span><span class="sxs-lookup"><span data-stu-id="1807b-146">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="1807b-147">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="1807b-147">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[<span data-ttu-id="1807b-148">Attributo Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="1807b-148">The wire\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="1807b-149">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="1807b-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="1807b-150">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="1807b-150">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="1807b-151">**\_marshalling utente**</span><span class="sxs-lookup"><span data-stu-id="1807b-151">**user\_marshal**</span></span>](user-marshal.md)
</dt> </dl>

 

 