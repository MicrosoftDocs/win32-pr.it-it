---
title: Funzione type_UserSize
description: Il tipo \_ UserSize Function è una funzione di supporto per gli attributi \ Wire \_ Marshal \ e \ User \_ Marshal \.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730018"
---
# <a name="the-type_usersize-function"></a><span data-ttu-id="f025d-104">Funzione di tipo \_ UserSize</span><span class="sxs-lookup"><span data-stu-id="f025d-104">The type\_UserSize Function</span></span>

<span data-ttu-id="f025d-105">La funzione **<type> \_ UserSize** è una funzione di supporto per il \[ [ \_ marshalling di rete](/windows/desktop/Midl/wire-marshal) \] e \[ gli attributi del [ \_ marshalling degli utenti](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="f025d-105">The **<type>\_UserSize** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="f025d-106">Gli stub chiamano questa funzione per ridimensionare il buffer di dati RPC per l'oggetto dati utente prima che venga eseguito il marshalling dei dati sul lato client o server.</span><span class="sxs-lookup"><span data-stu-id="f025d-106">The stubs call this function to size the RPC data buffer for the user data object before the data is marshaled on the client or server side.</span></span> <span data-ttu-id="f025d-107">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="f025d-107">The function is defined as:</span></span>

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

<span data-ttu-id="f025d-108"><type>Nel nome della funzione corrisponde a User-Type, come specificato nella definizione del **\[ \_ marshalling \] di rete** o del tipo di **\[ \_ \] marshalling dell'utente** .</span><span class="sxs-lookup"><span data-stu-id="f025d-108">The <type> in the function name means the userm-type, as specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="f025d-109">Questo tipo può essere untransmittable o even, se usato con l'attributo **\[ \_ Marshal \] dell'utente** , sconosciuto al compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="f025d-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute— unknown to the MIDL compiler.</span></span> <span data-ttu-id="f025d-110">Il nome del tipo Wire (il nome del tipo trasmesso attraverso la rete) non viene utilizzato nel prototipo di funzione.</span><span class="sxs-lookup"><span data-stu-id="f025d-110">The wire type name (the name of the type transmitted across the network) is not used in the function prototype.</span></span> <span data-ttu-id="f025d-111">Si noti, tuttavia, che il tipo Wire definisce il layout per i dati come specificato da OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="f025d-111">Note, however, that the wire type defines the layout for the data as specified by OSF DCE.</span></span> <span data-ttu-id="f025d-112">Tutti i dati devono essere convertiti nel formato di rappresentazione dei dati di rete (NDR).</span><span class="sxs-lookup"><span data-stu-id="f025d-112">All data must be converted to network data representation (NDR) format.</span></span>

<span data-ttu-id="f025d-113">Il parametro *pFlags* è un puntatore a un campo **unsigned long** flag.</span><span class="sxs-lookup"><span data-stu-id="f025d-113">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="f025d-114">La parola superiore del flag contiene i flag di formato NDR come definito da OSF DCE per la virgola mobile, l'ordine dei byte e le rappresentazioni di caratteri.</span><span class="sxs-lookup"><span data-stu-id="f025d-114">The upper word of the flag contains NDR format flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="f025d-115">La parola inferiore contiene un flag di contesto di marshalling definito dal canale COM.</span><span class="sxs-lookup"><span data-stu-id="f025d-115">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="f025d-116">La tabella seguente illustra il layout esatto dei flag all'interno del campo.</span><span class="sxs-lookup"><span data-stu-id="f025d-116">The exact layout of the flags within the field is shown in the following table.</span></span>



| <span data-ttu-id="f025d-117">BITS</span><span class="sxs-lookup"><span data-stu-id="f025d-117">Bits</span></span>  | <span data-ttu-id="f025d-118">Flag</span><span class="sxs-lookup"><span data-stu-id="f025d-118">Flag</span></span>                                  | <span data-ttu-id="f025d-119">valore</span><span class="sxs-lookup"><span data-stu-id="f025d-119">Value</span></span>                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f025d-120">31-24</span><span class="sxs-lookup"><span data-stu-id="f025d-120">31-24</span></span> | <span data-ttu-id="f025d-121">Rappresentazione a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="f025d-121">Floating-point representation</span></span>         | <span data-ttu-id="f025d-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span><span class="sxs-lookup"><span data-stu-id="f025d-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span></span>                                                         |
| <span data-ttu-id="f025d-123">23-20</span><span class="sxs-lookup"><span data-stu-id="f025d-123">23-20</span></span> | <span data-ttu-id="f025d-124">Ordine di byte Integer e a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="f025d-124">Integer and floating-point byte order</span></span> | <span data-ttu-id="f025d-125">0 = big-endian 1 = little-endian</span><span class="sxs-lookup"><span data-stu-id="f025d-125">0 = Big-endian 1 = Little-endian</span></span>                                                          |
| <span data-ttu-id="f025d-126">19-16</span><span class="sxs-lookup"><span data-stu-id="f025d-126">19-16</span></span> | <span data-ttu-id="f025d-127">Rappresentazione di caratteri</span><span class="sxs-lookup"><span data-stu-id="f025d-127">Character representation</span></span>              | <span data-ttu-id="f025d-128">0 = ASCII 1 = EBCDIC</span><span class="sxs-lookup"><span data-stu-id="f025d-128">0 = ASCII 1 = EBCDIC</span></span>                                                                      |
| <span data-ttu-id="f025d-129">15-0</span><span class="sxs-lookup"><span data-stu-id="f025d-129">15-0</span></span>  | <span data-ttu-id="f025d-130">Flag di contesto di marshalling</span><span class="sxs-lookup"><span data-stu-id="f025d-130">Marshaling context flag</span></span>               | <span data-ttu-id="f025d-131">0 = MSHCTX \_ Local 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ InProc</span><span class="sxs-lookup"><span data-stu-id="f025d-131">0 = MSHCTX\_LOCAL 1 = MSHCTX\_NOSHAREDMEM 2 = MSHCTX\_DIFFERENTMACHINE 3 = MSHCTX\_INPROC</span></span> |



 

<span data-ttu-id="f025d-132">Il flag di contesto del marshalling rende possibile la modifica del comportamento della routine a seconda del contesto della chiamata RPC.</span><span class="sxs-lookup"><span data-stu-id="f025d-132">The marshaling context flag makes it possible to alter the behavior of your routine depending on the context for the RPC call.</span></span> <span data-ttu-id="f025d-133">Se, ad esempio, si dispone di un handle (**Long**) per un blocco di dati, è possibile inviare l'handle per una chiamata in-process, ma inviare i dati effettivi per una chiamata a un altro computer.</span><span class="sxs-lookup"><span data-stu-id="f025d-133">For example, if you have a handle (**long**) to a block of data, you could send the handle for an in-process call, but you would send the actual data for a call to a different machine.</span></span> <span data-ttu-id="f025d-134">Il flag del contesto di marshalling e i relativi valori sono definiti nei file wtypes. h e wtypes. idl di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f025d-134">The marshaling context flag and its values are defined in the Wtypes.h and Wtypes.idl files in the Platform Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="f025d-135">Quando il tipo di trasmissione è definito correttamente, non è necessario usare i flag di formato NDR, perché il motore di NDR esegue le conversioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="f025d-135">When the wire type is properly defined, you do not have to use the NDR format flags, as the NDR engine performs the necessary conversions.</span></span>

 

<span data-ttu-id="f025d-136">*StartingSize* un parametro è l'offset del buffer corrente.</span><span class="sxs-lookup"><span data-stu-id="f025d-136">The *StartingSize* a parameter is the current buffer offset.</span></span> <span data-ttu-id="f025d-137">La dimensione iniziale indica l'offset del buffer per l'oggetto utente e può essere allineato o meno correttamente.</span><span class="sxs-lookup"><span data-stu-id="f025d-137">The starting size indicates the buffer offset for the user object, and it may or may not be aligned properly.</span></span> <span data-ttu-id="f025d-138">La routine dovrebbe tenere conto del riempimento necessario.</span><span class="sxs-lookup"><span data-stu-id="f025d-138">Your routine should account for whatever padding is necessary.</span></span>

<span data-ttu-id="f025d-139">Il parametro *pMyObj* è un puntatore a un oggetto tipo utente.</span><span class="sxs-lookup"><span data-stu-id="f025d-139">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="f025d-140">Il valore restituito è il nuovo offset o la nuova posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="f025d-140">The return value is the new offset or buffer position.</span></span> <span data-ttu-id="f025d-141">La funzione deve restituire la dimensione cumulativa, ovvero le dimensioni iniziali più la spaziatura interna più la dimensione dei dati.</span><span class="sxs-lookup"><span data-stu-id="f025d-141">The function should return the cumulative size, which is the starting size plus possible padding plus the data size.</span></span>

<span data-ttu-id="f025d-142">La funzione **<type> \_ UserSize** può restituire una sovrastima delle dimensioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="f025d-142">The **<type>\_UserSize** function can return an overestimate of the size needed.</span></span> <span data-ttu-id="f025d-143">La dimensione effettiva del buffer inviato è definita dalle dimensioni dei dati, non dalle dimensioni di allocazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="f025d-143">The actual size of the sent buffer is defined by the data size, not by the buffer allocation size.</span></span>

<span data-ttu-id="f025d-144">La funzione **<type> \_ UserSize** non viene chiamata se le dimensioni del Wire possono essere calcolate in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="f025d-144">The **<type>\_UserSize** function is not called if the wire size can be computed at compile time.</span></span> <span data-ttu-id="f025d-145">Si noti che per la maggior parte delle unioni, anche se non sono presenti puntatori, le dimensioni effettive della rappresentazione in transito possono essere determinate solo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f025d-145">Note that for most unions, even if there are no pointers, the actual size of the wire representation can be determined only at run time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f025d-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f025d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f025d-147">Regole di marshalling per \_ marshalling utente e \_ marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="f025d-147">Marshaling rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="f025d-148">\_marshalling utente</span><span class="sxs-lookup"><span data-stu-id="f025d-148">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="f025d-149">\_marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="f025d-149">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 