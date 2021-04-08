---
title: Funzione type_UserUnmarshal
description: Il tipo \_ UserUnmarshal Function è una funzione di supporto per gli attributi \ Wire \_ Marshal \ e \ User \_ Marshal \.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047319"
---
# <a name="the-type_userunmarshal-function"></a><span data-ttu-id="b0ccc-104">Funzione di tipo \_ UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="b0ccc-104">The type\_UserUnmarshal Function</span></span>

<span data-ttu-id="b0ccc-105">La funzione **<type> \_ UserUnmarshal** è una funzione di supporto per il \[ [ \_ marshalling di rete](/windows/desktop/Midl/wire-marshal) \] e \[ gli attributi del [ \_ marshalling degli utenti](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="b0ccc-105">The **<type>\_UserUnmarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="b0ccc-106">Gli stub chiamano questa funzione per eseguire l'unmarshalling dei dati sul lato client o server.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-106">The stubs call this function to unmarshal data on the client or server side.</span></span> <span data-ttu-id="b0ccc-107">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="b0ccc-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="b0ccc-108"><type>Nel nome della funzione indica il tipo di utente specificato nella definizione del **\[ \_ marshalling \] di rete** o del tipo di **\[ \_ \] marshalling dell'utente** .</span><span class="sxs-lookup"><span data-stu-id="b0ccc-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="b0ccc-109">Questo tipo può essere untransmittable o even, se usato con l'attributo **\[ \_ Marshal \] dell'utente** , sconosciuto al compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—unknown to the MIDL compiler.</span></span> <span data-ttu-id="b0ccc-110">Il nome del tipo Wire (il nome del tipo trasmissibile) non viene usato nel prototipo di funzione.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="b0ccc-111">Si noti, tuttavia, che il tipo Wire definisce il layout Wire per i dati come specificato da OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="b0ccc-112">Il parametro *pFlags* è un puntatore a un campo **unsigned long** flag.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-112">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="b0ccc-113">La parola superiore del flag contiene i flag di rappresentazione dei dati NDR come definito da OSF DCE per la virgola mobile, l'ordine dei byte e le rappresentazioni di caratteri.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="b0ccc-114">La parola inferiore contiene un flag di contesto di marshalling definito dal canale COM.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="b0ccc-115">Il layout esatto dei flag all'interno del campo viene descritto nella [funzione di tipo \_ UserSize](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="b0ccc-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="b0ccc-116">Il parametro *pbuffer* è il puntatore del buffer corrente.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="b0ccc-117">Il puntatore potrebbe non essere allineato alla voce.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="b0ccc-118">La funzione **<type> \_ UserUnmarshal** deve allineare il puntatore del buffer in modo appropriato, annullare il marshalling dei dati e restituire la nuova posizione del buffer, ovvero l'indirizzo del primo byte dopo l'oggetto di cui è stato eseguito l'unmarshalling.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-118">Your **<type>\_UserUnmarshal** function should align the buffer pointer appropriately, unmarshal the data, and return the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="b0ccc-119">Il parametro *pMyObj* è un puntatore a un oggetto di tipo definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-119">The *pMyObj* parameter is a pointer to a user-defined type object.</span></span>

<span data-ttu-id="b0ccc-120">In un ambiente eterogeneo, il motore NDR esegue qualsiasi conversione dei dati necessaria prima di chiamare la funzione **<type> \_ UserUnmarshal** .</span><span class="sxs-lookup"><span data-stu-id="b0ccc-120">In a heterogeneous environment, the NDR engine performs any data conversion necessary before calling the **<type>\_UserUnmarshal** function.</span></span> <span data-ttu-id="b0ccc-121">Si noti che il motore di NDR esegue questa conversione dei dati in base alla definizione di tipo Wire specificata per questo tipo di dati utente.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-121">Note that the NDR engine carries out this data conversion according to the wire-type definition supplied for this user data type.</span></span> <span data-ttu-id="b0ccc-122">Il flag indica la rappresentazione dati del mittente.</span><span class="sxs-lookup"><span data-stu-id="b0ccc-122">The flag indicates the data representation of the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0ccc-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0ccc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0ccc-124">Regole di marshalling per \_ marshalling utente e \_ marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="b0ccc-124">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="b0ccc-125">\_marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="b0ccc-125">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="b0ccc-126">\_marshalling utente</span><span class="sxs-lookup"><span data-stu-id="b0ccc-126">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 