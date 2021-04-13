---
title: Funzione type_UserMarshal
description: Il tipo \_ UserMarshal Function è una funzione di supporto per gli attributi \ Wire \_ Marshal \ e \ User \_ Marshal \.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399685"
---
# <a name="the-type_usermarshal-function"></a><span data-ttu-id="e4415-104">Funzione di tipo \_ UserMarshal</span><span class="sxs-lookup"><span data-stu-id="e4415-104">The type\_UserMarshal Function</span></span>

<span data-ttu-id="e4415-105">La funzione **<type> \_ UserMarshal** è una funzione di supporto per il \[ [ \_ marshalling di rete](/windows/desktop/Midl/wire-marshal) \] e \[ gli attributi del [ \_ marshalling degli utenti](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="e4415-105">The **<type>\_UserMarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="e4415-106">Gli stub chiamano questa funzione per effettuare il marshalling dei dati sul lato client o server.</span><span class="sxs-lookup"><span data-stu-id="e4415-106">The stubs call this function to marshal data on the client or server side.</span></span> <span data-ttu-id="e4415-107">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="e4415-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="e4415-108"><type>Nel nome della funzione indica il tipo di utente specificato nella definizione del **\[ \_ marshalling \] di rete** o del tipo di **\[ \_ \] marshalling dell'utente** .</span><span class="sxs-lookup"><span data-stu-id="e4415-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="e4415-109">Questo tipo può essere untransmittable o even, se usato con l'attributo **\[ \_ Marshal \] utente** , un tipo sconosciuto al compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="e4415-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—a type unknown to the MIDL compiler.</span></span> <span data-ttu-id="e4415-110">Il nome del tipo Wire (il nome del tipo trasmissibile) non viene usato nel prototipo di funzione.</span><span class="sxs-lookup"><span data-stu-id="e4415-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="e4415-111">Si noti, tuttavia, che il tipo Wire definisce il layout Wire per i dati come specificato da OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="e4415-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="e4415-112">Il parametro *pFlags* è un puntatore a un campo unsigned long flag.</span><span class="sxs-lookup"><span data-stu-id="e4415-112">The *pFlags* parameter is a pointer to an unsigned long flag field.</span></span> <span data-ttu-id="e4415-113">La parola superiore del flag contiene i flag di rappresentazione dei dati NDR come definito da OSF DCE per la virgola mobile, l'ordine dei byte e le rappresentazioni di caratteri.</span><span class="sxs-lookup"><span data-stu-id="e4415-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="e4415-114">La parola inferiore contiene un flag di contesto di marshalling definito dal canale COM.</span><span class="sxs-lookup"><span data-stu-id="e4415-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="e4415-115">Il layout esatto dei flag all'interno del campo viene descritto nella [funzione di tipo \_ UserSize](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="e4415-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="e4415-116">Il parametro *pbuffer* è il puntatore del buffer corrente.</span><span class="sxs-lookup"><span data-stu-id="e4415-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="e4415-117">Il puntatore potrebbe non essere allineato alla voce.</span><span class="sxs-lookup"><span data-stu-id="e4415-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="e4415-118">La funzione **<type> \_ UserMarshal** deve allineare il puntatore del buffer in modo appropriato, effettuare il marshalling dei dati e restituire la nuova posizione del buffer, ovvero l'indirizzo del primo byte dopo l'oggetto di cui è stato effettuato il marshalling.</span><span class="sxs-lookup"><span data-stu-id="e4415-118">Your **<type>\_UserMarshal** function should align the buffer pointer appropriately, marshal the data, and return the new buffer position, which is the address of the first byte after the marshaled object.</span></span> <span data-ttu-id="e4415-119">Tenere presente che la specifica del tipo Wire determina il layout effettivo dei dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="e4415-119">Keep in mind that the wire type specification determines the actual layout of the data in the buffer.</span></span>

<span data-ttu-id="e4415-120">Il parametro *pMyObj* è un puntatore a un oggetto tipo utente.</span><span class="sxs-lookup"><span data-stu-id="e4415-120">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="e4415-121">Il valore restituito è la nuova posizione del buffer, ovvero l'indirizzo del primo byte dopo l'oggetto di cui è stato eseguito l'unmarshalling.</span><span class="sxs-lookup"><span data-stu-id="e4415-121">The return value is the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="e4415-122">L'overflow del buffer può verificarsi quando si calcolano erroneamente le dimensioni dei dati e si tenta di effettuare il marshalling di più dati del previsto.</span><span class="sxs-lookup"><span data-stu-id="e4415-122">Buffer overflow can occur when you incorrectly calculate the size of the data and attempt to marshal more data than expected.</span></span> <span data-ttu-id="e4415-123">È necessario prestare attenzione per evitare questa situazione.</span><span class="sxs-lookup"><span data-stu-id="e4415-123">You should be careful to avoid this situation.</span></span> <span data-ttu-id="e4415-124">Per verificarlo, è possibile usare il puntatore restituito da **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="e4415-124">You can check against it by using the pointer that **<type>\_UserMarshal** returns.</span></span> <span data-ttu-id="e4415-125">In caso contrario, si rischia che il motore di NDR generi un'eccezione di overflow del buffer in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="e4415-125">Otherwise, you risk having the NDR engine raise a buffer-overflow exception later.</span></span>

<span data-ttu-id="e4415-126">Le eccezioni devono essere rilevate e gestite localmente, le eccezioni non devono essere consentite per propigated lo stack di chiamate.</span><span class="sxs-lookup"><span data-stu-id="e4415-126">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4415-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4415-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4415-128">Regole di marshalling per \_ marshalling utente e \_ marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="e4415-128">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="e4415-129">\_marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="e4415-129">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="e4415-130">\_marshalling utente</span><span class="sxs-lookup"><span data-stu-id="e4415-130">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 