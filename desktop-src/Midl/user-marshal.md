---
title: attributo user_marshal
description: L' \_ attributo ACF del marshalling dell'utente associa un tipo locale denominato al linguaggio di destinazione (User-Type) con un tipo di trasferimento (tipo Wire) che viene trasferito tra il client e il server.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- attributo user_marshal MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337023"
---
# <a name="user_marshal-attribute"></a><span data-ttu-id="f89cc-104">\_attributo Marshal utente</span><span class="sxs-lookup"><span data-stu-id="f89cc-104">user\_marshal attribute</span></span>

<span data-ttu-id="f89cc-105">L'attributo ACF del **\_ marshalling dell'utente** associa un tipo locale denominato al linguaggio di destinazione (*User-Type*) con un tipo di trasferimento (*tipo Wire*) che viene trasferito tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="f89cc-105">The **user\_marshal** ACF attribute associates a named local type in the target language (*userm-type*) with a transfer type (*wire-type*) that is transferred between client and server.</span></span>

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="f89cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f89cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f89cc-107">*utente-tipo*</span><span class="sxs-lookup"><span data-stu-id="f89cc-107">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f89cc-108">Specifica l'identificatore del tipo di dati utente di cui effettuare il marshalling.</span><span class="sxs-lookup"><span data-stu-id="f89cc-108">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="f89cc-109">Il *tipo di utente* non deve essere trasmissibile e non deve essere un tipo noto al compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="f89cc-109">The *userm-type* need not be transmittable and need not be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="f89cc-110">*tipo Wire*</span><span class="sxs-lookup"><span data-stu-id="f89cc-110">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f89cc-111">Specifica il tipo di dati di trasferimento denominato effettivamente trasferito tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="f89cc-111">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="f89cc-112">Il tipo Wire deve essere un tipo di base MIDL, un tipo predefinito o un identificatore di tipo di un tipo che può essere trasmesso attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="f89cc-112">The wire type must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="f89cc-113">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="f89cc-113">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="f89cc-114">Specifica un puntatore a un campo del flag ( [**Long**](long.md) [**senza segno**](unsigned.md) ).</span><span class="sxs-lookup"><span data-stu-id="f89cc-114">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="f89cc-115">La parola più significativa specifica i flag di rappresentazione dei dati NDR come definito da DCE per la rappresentazione a virgola mobile, Big o little-endian e character.</span><span class="sxs-lookup"><span data-stu-id="f89cc-115">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="f89cc-116">La parola di ordine inferiore specifica un flag di contesto di marshalling.</span><span class="sxs-lookup"><span data-stu-id="f89cc-116">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="f89cc-117">Il layout esatto dei flag viene descritto nella [funzione di tipo \_ UserSize](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="f89cc-117">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="f89cc-118">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="f89cc-118">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f89cc-119">Specifica la dimensione del buffer corrente (offset) prima di ridimensionare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f89cc-119">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="f89cc-120">*\_TypeObject Puser*</span><span class="sxs-lookup"><span data-stu-id="f89cc-120">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="f89cc-121">Specifica un puntatore a un oggetto di *\_ tipo User*.</span><span class="sxs-lookup"><span data-stu-id="f89cc-121">Specifies a pointer to an object of *userm\_type*.</span></span>

</dd> <dt>

<span data-ttu-id="f89cc-122">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="f89cc-122">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f89cc-123">Specifica il puntatore al buffer corrente.</span><span class="sxs-lookup"><span data-stu-id="f89cc-123">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f89cc-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="f89cc-124">Remarks</span></span>

<span data-ttu-id="f89cc-125">Ogni tipo locale denominato, *User-Type*, presenta una corrispondenza uno-a-uno con un *tipo Wire* che definisce la rappresentazione in transito del tipo.</span><span class="sxs-lookup"><span data-stu-id="f89cc-125">Each named local type, *userm-type*, has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="f89cc-126">È necessario specificare routine per dimensionare i dati per il marshalling, per effettuare il marshalling e l'unmarshalling dei dati e per liberare memoria.</span><span class="sxs-lookup"><span data-stu-id="f89cc-126">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="f89cc-127">Per ulteriori informazioni su queste routine, vedere [l' \_ attributo Marshal utente](/windows/desktop/Rpc/the-user-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="f89cc-127">For more information on these routines, see [The user\_marshal Attribute](/windows/desktop/Rpc/the-user-marshal-attribute).</span></span> <span data-ttu-id="f89cc-128">Si noti che se nei dati sono presenti tipi incorporati che sono definiti anche **con \_ marshalling utente** o \[ [**\[ \_ marshalling \] di rete**](wire-marshal.md), è necessario gestire anche la manutenzione di tali tipi incorporati.</span><span class="sxs-lookup"><span data-stu-id="f89cc-128">Note that if there are embedded types in your data that are also defined with **user\_marshal** or \[ [**\[wire\_marshal\]**](wire-marshal.md), you need to manage the servicing of those embedded types also.</span></span>

<span data-ttu-id="f89cc-129">Il *tipo di collegamento* non può essere un puntatore di interfaccia o un puntatore completo.</span><span class="sxs-lookup"><span data-stu-id="f89cc-129">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="f89cc-130">Il *tipo di Wire* deve avere una dimensione di memoria ben definita.</span><span class="sxs-lookup"><span data-stu-id="f89cc-130">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="f89cc-131">Per informazioni dettagliate su come effettuare il marshalling di un determinato *tipo di Wire*, vedere [regole di marshalling per \_ marshalling degli utenti e \_ marshalling di rete](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .</span><span class="sxs-lookup"><span data-stu-id="f89cc-131">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="f89cc-132">Il *tipo di utente* non deve essere un puntatore di interfaccia perché è possibile effettuare il marshalling direttamente.</span><span class="sxs-lookup"><span data-stu-id="f89cc-132">The *userm-type* should not be an interface pointer as these can be marshaled directly.</span></span> <span data-ttu-id="f89cc-133">Se il tipo di utente è un puntatore completo, è necessario gestire manualmente l'alias.</span><span class="sxs-lookup"><span data-stu-id="f89cc-133">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

## <a name="examples"></a><span data-ttu-id="f89cc-134">Esempi</span><span class="sxs-lookup"><span data-stu-id="f89cc-134">Examples</span></span>

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a><span data-ttu-id="f89cc-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f89cc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f89cc-136">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="f89cc-136">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="f89cc-137">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="f89cc-137">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="f89cc-138">**long**</span><span class="sxs-lookup"><span data-stu-id="f89cc-138">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="f89cc-139">**rappresenta \_ come**</span><span class="sxs-lookup"><span data-stu-id="f89cc-139">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="f89cc-140">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="f89cc-140">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="f89cc-141">\_Attributo Marshal utente</span><span class="sxs-lookup"><span data-stu-id="f89cc-141">The user\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="f89cc-142">**\_marshalling di rete**</span><span class="sxs-lookup"><span data-stu-id="f89cc-142">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="f89cc-143">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="f89cc-143">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 