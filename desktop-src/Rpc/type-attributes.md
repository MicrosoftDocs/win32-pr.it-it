---
title: Attributi di tipo
description: Remote Procedure Call (RPC) e gli attributi di tipo MIDL che possono essere applicati alle dichiarazioni di tipo.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872549"
---
# <a name="type-attributes"></a><span data-ttu-id="ce2e2-103">Attributi di tipo</span><span class="sxs-lookup"><span data-stu-id="ce2e2-103">Type Attributes</span></span>

<span data-ttu-id="ce2e2-104">Gli attributi di tipo sono gli attributi MIDL che è possibile applicare alle dichiarazioni di tipo:</span><span class="sxs-lookup"><span data-stu-id="ce2e2-104">Type attributes are the MIDL attributes that can be applied to type declarations:</span></span>

-   <span data-ttu-id="ce2e2-105">**\[**[**gestire**](/windows/desktop/Midl/handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="ce2e2-105">**\[**[**handle**](/windows/desktop/Midl/handle)**\]**</span></span>
-   <span data-ttu-id="ce2e2-106">**\[**[**handle di contesto \_**](/windows/desktop/Midl/context-handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="ce2e2-106">**\[**[**context\_handle**](/windows/desktop/Midl/context-handle)**\]**</span></span>
-   <span data-ttu-id="ce2e2-107">**\[**[**tipo di opzione \_**](/windows/desktop/Midl/switch-type)**\]**</span><span class="sxs-lookup"><span data-stu-id="ce2e2-107">**\[**[**switch\_type**](/windows/desktop/Midl/switch-type)**\]**</span></span>
-   [<span data-ttu-id="ce2e2-108">attributi di tipo puntatore</span><span class="sxs-lookup"><span data-stu-id="ce2e2-108">pointer type attributes</span></span>](three-pointer-types.md)

<span data-ttu-id="ce2e2-109">L'attributo **\[ Switch \_ Type \]** designa il tipo di un discriminatore di Unione.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-109">The **\[switch\_type\]** attribute designates the type of a union discriminator.</span></span> <span data-ttu-id="ce2e2-110">Questo attributo si applica solo a un'Unione non incapsulata.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-110">This attribute applies only to a nonencapsulated union.</span></span>

<span data-ttu-id="ce2e2-111">Un handle di contesto è un puntatore con un attributo dell' **\[ \_ handle \] di contesto** .</span><span class="sxs-lookup"><span data-stu-id="ce2e2-111">A context handle is a pointer with a **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="ce2e2-112">L'attributo **\[ \_ handle \] di contesto** consente di scrivere procedure per la gestione delle informazioni sullo stato tra le chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-112">The **\[context\_handle\]** attribute allows you to write procedures that maintain state information between remote procedure calls.</span></span> <span data-ttu-id="ce2e2-113">Un handle di contesto con un valore non null rappresenta il contesto salvato e serve due scopi:</span><span class="sxs-lookup"><span data-stu-id="ce2e2-113">A context handle with a non-null value represents saved context and serves two purposes:</span></span>

-   <span data-ttu-id="ce2e2-114">Sul lato client, contiene le informazioni richieste dalla libreria di runtime RPC per indirizzare la chiamata al server.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-114">On the client side, it contains the information needed by the RPC run-time library to direct the call to the server.</span></span>
-   <span data-ttu-id="ce2e2-115">Sul lato server, funge da handle nel contesto attivo.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-115">On the server side, it serves as a handle on active context.</span></span>

<span data-ttu-id="ce2e2-116">L' **\[** [](/windows/desktop/Midl/handle) **\]** attributo handle specifica che un tipo può verificarsi come handle definito dall'utente (generico).</span><span class="sxs-lookup"><span data-stu-id="ce2e2-116">The **\[**[**handle**](/windows/desktop/Midl/handle)**\]** attribute specifies that a type can occur as a user-defined (generic) handle.</span></span> <span data-ttu-id="ce2e2-117">Questa funzionalità consente la progettazione di handle significativi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-117">This feature permits the design of handles that are meaningful to the application.</span></span> <span data-ttu-id="ce2e2-118">L'utente deve fornire routine di binding e di annullamento dell'associazione per eseguire la conversione tra il tipo di handle definito dall'utente e il tipo di handle della primitiva RPC, **handle \_ t**.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-118">The user must provide binding and unbinding routines to convert between the user-defined handle type and the RPC primitive handle type, **handle\_t**.</span></span> <span data-ttu-id="ce2e2-119">Un handle primitivo contiene informazioni sulla destinazione significative per le librerie di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-119">A primitive handle contains destination information meaningful to the RPC run-time libraries.</span></span> <span data-ttu-id="ce2e2-120">Un handle definito dall'utente può essere definito solo in una dichiarazione di tipo, non in una dichiarazione di funzione.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-120">A user-defined handle can only be defined in a type declaration, not in a function declaration.</span></span> <span data-ttu-id="ce2e2-121">Un parametro con l'attributo **\[ handle \]** ha un doppio scopo.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-121">A parameter with the **\[handle\]** attribute has a double purpose.</span></span> <span data-ttu-id="ce2e2-122">Viene utilizzato per determinare il binding per la chiamata e viene trasmesso alla routine chiamata come parametro dati normale.</span><span class="sxs-lookup"><span data-stu-id="ce2e2-122">It is used to determine the binding for the call, and it is transmitted to the called procedure as a normal data parameter.</span></span>

 

 