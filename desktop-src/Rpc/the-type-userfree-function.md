---
title: Funzione type_UserFree
description: Il tipo \_ UserFree Function è una funzione di supporto per gli attributi \ Wire \_ Marshal \ e \ User \_ Marshal \.
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727442"
---
# <a name="the-type_userfree-function"></a><span data-ttu-id="61f89-104">Funzione di tipo \_ UserFree</span><span class="sxs-lookup"><span data-stu-id="61f89-104">The type\_UserFree Function</span></span>

<span data-ttu-id="61f89-105">La funzione **<type> \_ UserFree** è una funzione di supporto per il \[ [ \_ marshalling di rete](/windows/desktop/Midl/wire-marshal) \] e \[ gli attributi del [ \_ marshalling degli utenti](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="61f89-105">The **<type>\_UserFree** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="61f89-106">Gli stub chiamano questa funzione per liberare i dati sul lato server.</span><span class="sxs-lookup"><span data-stu-id="61f89-106">The stubs call this function to free the data on the server side.</span></span> <span data-ttu-id="61f89-107">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="61f89-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

<span data-ttu-id="61f89-108"><type>Nel nome della funzione indica il tipo di utente specificato nella definizione del **\[ \_ marshalling \] di rete** o del tipo di **\[ \_ \] marshalling dell'utente** .</span><span class="sxs-lookup"><span data-stu-id="61f89-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span>

<span data-ttu-id="61f89-109">Il parametro *pFlags* è un puntatore a un campo **unsigned long** flag.</span><span class="sxs-lookup"><span data-stu-id="61f89-109">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="61f89-110">La parola superiore del flag contiene i flag di rappresentazione dei dati NDR come definito da OSF DCE per la virgola mobile, l'ordine dei byte e le rappresentazioni di caratteri.</span><span class="sxs-lookup"><span data-stu-id="61f89-110">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="61f89-111">La parola inferiore contiene un flag di contesto di marshalling definito dal canale COM.</span><span class="sxs-lookup"><span data-stu-id="61f89-111">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="61f89-112">Il layout esatto dei flag all'interno del campo viene descritto nella [funzione di tipo \_ UserSize](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="61f89-112">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="61f89-113">Il parametro *pMyObj* è un puntatore a un oggetto tipo utente.</span><span class="sxs-lookup"><span data-stu-id="61f89-113">The *pMyObj* parameter is a pointer to a user type object.</span></span> <span data-ttu-id="61f89-114">Il motore NDR libera l'oggetto di primo livello.</span><span class="sxs-lookup"><span data-stu-id="61f89-114">The NDR engine frees the top-level object.</span></span> <span data-ttu-id="61f89-115">L'utente è responsabile di liberare tutti gli oggetti a cui può puntare l'oggetto di primo livello.</span><span class="sxs-lookup"><span data-stu-id="61f89-115">You are responsible for freeing any objects to which the top-level object may point.</span></span>

<span data-ttu-id="61f89-116">Le eccezioni devono essere rilevate e gestite localmente, le eccezioni non devono essere consentite per propigated lo stack di chiamate.</span><span class="sxs-lookup"><span data-stu-id="61f89-116">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61f89-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61f89-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61f89-118">Regole di marshalling per \_ marshalling utente e \_ marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="61f89-118">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="61f89-119">\_marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="61f89-119">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="61f89-120">\_marshalling utente</span><span class="sxs-lookup"><span data-stu-id="61f89-120">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 