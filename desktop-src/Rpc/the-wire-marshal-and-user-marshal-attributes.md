---
title: Attributi wire_marshal e user_marshal
description: In questa sezione viene illustrata l'implementazione della conversione dei tipi di dati del programmatore mediante gli attributi MIDL \ Wire \_ Marshal \ e \ User \_ Marshal \.
ms.assetid: 0ee2ce86-cd14-4659-a69f-6336145359da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a789f11fa15a20eab0fcd468cc410bb5a7200717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047158"
---
# <a name="the-wire_marshal-and-user_marshal-attributes"></a><span data-ttu-id="92d75-103">\_Attributi di marshalling di rete e di \_ marshalling degli utenti</span><span class="sxs-lookup"><span data-stu-id="92d75-103">The wire\_marshal and user\_marshal Attributes</span></span>

<span data-ttu-id="92d75-104">In questa sezione viene illustrata l'implementazione della conversione dei tipi di dati del programmatore utilizzando il \[ [ \_ marshalling Wire](/windows/desktop/Midl/wire-marshal) \] e \[ gli attributi di [ \_ marshalling degli utenti](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="92d75-104">This section discusses the implementation of programmer data type conversion using the MIDL \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="92d75-105">Le informazioni vengono presentate nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="92d75-105">The information is presented in the following sections:</span></span>

-   [<span data-ttu-id="92d75-106">Attributo Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="92d75-106">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
-   [<span data-ttu-id="92d75-107">\_Attributo Marshal utente</span><span class="sxs-lookup"><span data-stu-id="92d75-107">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
-   [<span data-ttu-id="92d75-108">Funzione di tipo \_ UserSize</span><span class="sxs-lookup"><span data-stu-id="92d75-108">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
-   [<span data-ttu-id="92d75-109">Funzione di tipo \_ UserMarshal</span><span class="sxs-lookup"><span data-stu-id="92d75-109">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
-   [<span data-ttu-id="92d75-110">Funzione di tipo \_ UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="92d75-110">The type\_UserUnmarshal Function</span></span>](the-type-userunmarshal-function.md)
-   [<span data-ttu-id="92d75-111">Funzione di tipo \_ UserFree</span><span class="sxs-lookup"><span data-stu-id="92d75-111">The type\_UserFree Function</span></span>](the-type-userfree-function.md)
-   [<span data-ttu-id="92d75-112">Regole di marshalling per \_ marshalling utente e \_ marshalling di rete</span><span class="sxs-lookup"><span data-stu-id="92d75-112">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)

 

 