---
title: Regole di marshalling per user_marshal e wire_marshal
description: La specifica OSF-DCE per il marshalling dei tipi di puntatore incorporato richiede di osservare le restrizioni seguenti quando si implementa il tipo \_ UserSize, digitare \_ UserMarshal e digitare \_ UserUnMarshal Functions.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728858"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a><span data-ttu-id="7f788-103">Regole di marshalling per \_ marshalling utente e \_ marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="7f788-103">Marshaling Rules for user\_marshal and wire\_marshal</span></span>

<span data-ttu-id="7f788-104">La specifica OSF-DCE per il marshalling dei tipi di puntatore incorporato richiede di osservare le restrizioni seguenti quando si implementano le <type> \_ funzioni UserSize, <type> \_ UserMarshal e <type> \_ UserUnMarshal.</span><span class="sxs-lookup"><span data-stu-id="7f788-104">The OSF-DCE specification for marshaling embedded pointer types requires that you observe the following restrictions when implementing the <type>\_UserSize, <type>\_UserMarshal, and <type>\_UserUnMarshal functions.</span></span> <span data-ttu-id="7f788-105">(Le regole e gli esempi riportati di seguito sono per il marshalling.</span><span class="sxs-lookup"><span data-stu-id="7f788-105">(The rules and examples given here are for marshaling.</span></span> <span data-ttu-id="7f788-106">Tuttavia, le routine di ridimensionamento e di unmarshalling devono rispettare le stesse restrizioni:</span><span class="sxs-lookup"><span data-stu-id="7f788-106">However, your sizing and unmarshaling routines must follow the same restrictions):</span></span>

-   <span data-ttu-id="7f788-107">Se il tipo Wire è un tipo Flat senza puntatori, la routine di marshalling per il tipo User-Type corrispondente dovrebbe semplicemente effettuare il marshalling dei dati in base al layout del tipo di Wire.</span><span class="sxs-lookup"><span data-stu-id="7f788-107">If the wire-type is a flat type with no pointers, your marshaling routine for the corresponding userm-type should simply marshal the data according to the layout of the wire-type.</span></span> <span data-ttu-id="7f788-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="7f788-108">For example:</span></span>

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    <span data-ttu-id="7f788-109">Si noti che il tipo Wire, **Long**, è un tipo flat.</span><span class="sxs-lookup"><span data-stu-id="7f788-109">Note that the wire type, **long**, is a flat type.</span></span> <span data-ttu-id="7f788-110">Il gestore gestisce il \_ \_ marshalling della funzione UserMarshal a **lungo** ogni volta che un oggetto handle handle \_ viene passato a tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f788-110">Your HANDLE\_HANDLE\_UserMarshal function marshals a **long** whenever a HANDLE\_HANDLE object is passed to it.</span></span>

-   <span data-ttu-id="7f788-111">Se il tipo di Wire è un puntatore a un altro tipo, la routine di marshalling per il tipo di utente corrispondente deve effettuare il marshalling dei dati in base al layout per il tipo a cui punta il tipo di Wire.</span><span class="sxs-lookup"><span data-stu-id="7f788-111">If the wire-type is a pointer to another type, your marshaling routine for the corresponding userm-type should marshal the data according to the layout for the type that the wire-type points to.</span></span> <span data-ttu-id="7f788-112">Il motore di NDR si occupa dell'indicatore di misura.</span><span class="sxs-lookup"><span data-stu-id="7f788-112">The NDR engine takes care of the pointer.</span></span> <span data-ttu-id="7f788-113">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="7f788-113">For example:</span></span>

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    <span data-ttu-id="7f788-114">Si noti che il tipo di **trasmissione \_ Wire è** un tipo di puntatore.</span><span class="sxs-lookup"><span data-stu-id="7f788-114">Note that the wire type, **WIRE\_TYPE**, is a pointer type.</span></span> <span data-ttu-id="7f788-115">La \_ funzione UserMarshal data di handle esegue il \_ marshalling dei dati correlati all'handle, usando il layout HDATA anziché il \* layout HDATA.</span><span class="sxs-lookup"><span data-stu-id="7f788-115">Your HANDLE\_DATA\_UserMarshal function marshals the data related to the handle, using the HDATA layout, rather than the HDATA \* layout.</span></span>

-   <span data-ttu-id="7f788-116">Un tipo di collegamento deve essere un tipo di dati flat o un tipo di puntatore.</span><span class="sxs-lookup"><span data-stu-id="7f788-116">A wire-type must be either a flat data type or a pointer type.</span></span> <span data-ttu-id="7f788-117">Se il tipo trasmissibile deve essere un altro elemento (una struttura con puntatori, ad esempio), usare un puntatore al tipo desiderato come tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="7f788-117">If your transmissible type must be something else (a structure with pointers, for example), use a pointer to your desired type as the wire-type.</span></span>

<span data-ttu-id="7f788-118">L'effetto di queste restrizioni è che i tipi definiti con gli attributi di marshalling \[ [**\_**](/windows/desktop/Midl/wire-marshal) \] o di \[ [**\_ marshalling degli utenti**](/windows/desktop/Midl/user-marshal) \] possono essere incorporati liberamente in altri tipi.</span><span class="sxs-lookup"><span data-stu-id="7f788-118">The effect of these restrictions is that the types defined with the \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\] or \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\] attributes can be freely embedded in other types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f788-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f788-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f788-120">**\_marshalling di rete**</span><span class="sxs-lookup"><span data-stu-id="7f788-120">**wire\_marshal**</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="7f788-121">**\_marshalling utente**</span><span class="sxs-lookup"><span data-stu-id="7f788-121">**user\_marshal**</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="7f788-122">Funzione di tipo \_ UserSize</span><span class="sxs-lookup"><span data-stu-id="7f788-122">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
</dt> <dt>

[<span data-ttu-id="7f788-123">Funzione di tipo \_ UserMarshal</span><span class="sxs-lookup"><span data-stu-id="7f788-123">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
</dt> <dt>

[<span data-ttu-id="7f788-124">\_UserUnMarshalFunction thetype</span><span class="sxs-lookup"><span data-stu-id="7f788-124">Thetype\_UserUnMarshalFunction</span></span>](the-type-userunmarshal-function.md)
</dt> <dt>

[<span data-ttu-id="7f788-125">\_UserFreeFunction thetype</span><span class="sxs-lookup"><span data-stu-id="7f788-125">Thetype\_UserFreeFunction</span></span>](the-type-userfree-function.md)
</dt> </dl>

 

 