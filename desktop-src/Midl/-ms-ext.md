---
title: /ms_ext opzione
description: A partire da MIDL versione 3,0, le funzionalità abilitate dall' \_ opzione MS EXT sono ora la modalità predefinita per il compilatore MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext switch MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046600"
---
# <a name="ms_ext-switch"></a><span data-ttu-id="ed5a8-104">\_Switch EXT/MS</span><span class="sxs-lookup"><span data-stu-id="ed5a8-104">/ms\_ext switch</span></span>

<span data-ttu-id="ed5a8-105">A partire da MIDL versione 3,0, le funzionalità abilitate dall'opzione **MS \_ ext** sono ora la modalità predefinita per il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="ed5a8-105">Effective with MIDL version 3.0, the features enabled by the **ms\_ext** switch are now the default mode for the MIDL compiler.</span></span>

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a><span data-ttu-id="ed5a8-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="ed5a8-106">Switch Options</span></span>

<span data-ttu-id="ed5a8-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="ed5a8-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed5a8-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed5a8-108">Remarks</span></span>

<span data-ttu-id="ed5a8-109">Se si usa l'opzione, non verrà generato un errore del compilatore, pertanto non è necessario rimuovere i riferimenti a **/MS \_ ext** o [**/c \_ ext**](-c-ext.md) da un makefile esistente.</span><span class="sxs-lookup"><span data-stu-id="ed5a8-109">Using the switch will not generate a compiler error, so you do not have to remove references to **/ms\_ext** or [**/c\_ext**](-c-ext.md) from an existing makefile.</span></span>

<span data-ttu-id="ed5a8-110">Le estensioni Microsoft seguenti per OSF DCE sono ora disponibili per impostazione predefinita:</span><span class="sxs-lookup"><span data-stu-id="ed5a8-110">The following Microsoft extensions to OSF DCE are now available by default:</span></span>

-   <span data-ttu-id="ed5a8-111">Definizioni di interfaccia per gli oggetti OLE.</span><span class="sxs-lookup"><span data-stu-id="ed5a8-111">Interface definitions for OLE objects.</span></span> <span data-ttu-id="ed5a8-112">Per ulteriori informazioni sui file generati per le interfacce OLE, vedere [file generati per un'interfaccia com](files-generated-for-a-com-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ed5a8-112">For more information on the files generated for OLE interfaces, see [Files Generated for a COM Interface](files-generated-for-a-com-interface.md)</span></span>
-   <span data-ttu-id="ed5a8-113">Un attributo di [**\[ callback \]**](callback.md) che specifica una funzione di callback statica sul client</span><span class="sxs-lookup"><span data-stu-id="ed5a8-113">A [**\[callback\]**](callback.md) attribute specifying a static callback function on the client</span></span>
-   <span data-ttu-id="ed5a8-114">[**\_ virgolette cpp**](cpp-quote.md)(*\_ stringa tra virgolette*) e [**\# pragma MIDL \_ echo**](pragma.md)</span><span class="sxs-lookup"><span data-stu-id="ed5a8-114">[**cpp\_quote**](cpp-quote.md)(*quoted\_string*) and [**\#pragma midl\_echo**](pragma.md)</span></span>
-   <span data-ttu-id="ed5a8-115">tipi di caratteri wide, costanti e stringhe [**WCHAR \_ t**](wchar-t.md)</span><span class="sxs-lookup"><span data-stu-id="ed5a8-115">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings</span></span>
-   <span data-ttu-id="ed5a8-116">[**inizializzazione enum**](enum.md) (enumeratori sparse)</span><span class="sxs-lookup"><span data-stu-id="ed5a8-116">[**enum initialization**](enum.md) (sparse enumerators)</span></span>
-   <span data-ttu-id="ed5a8-117">Espressioni come identificatori di dimensioni e discriminatori</span><span class="sxs-lookup"><span data-stu-id="ed5a8-117">Expressions as size and discriminator specifiers</span></span>
-   [<span data-ttu-id="ed5a8-118">Gestisci estensioni</span><span class="sxs-lookup"><span data-stu-id="ed5a8-118">Handle extensions</span></span>](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [<span data-ttu-id="ed5a8-119">Puntatore-ereditarietà del tipo di attributo</span><span class="sxs-lookup"><span data-stu-id="ed5a8-119">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [<span data-ttu-id="ed5a8-120">Interfacce multiple</span><span class="sxs-lookup"><span data-stu-id="ed5a8-120">Multiple interfaces</span></span>](/windows/desktop/Rpc/registering-interfaces)
-   <span data-ttu-id="ed5a8-121">Definizioni all'esterno del blocco Interface</span><span class="sxs-lookup"><span data-stu-id="ed5a8-121">Definitions outside of the interface block</span></span>
-   <span data-ttu-id="ed5a8-122">È possibile omettere [gli attributi direzionali](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**in**](in.md), [**out**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="ed5a8-122">You can omit [directional attributes](/windows/desktop/Rpc/directional-parameter-attributes) \[[**in**](in.md), [**out**](out-idl.md)\]</span></span>

## <a name="see-also"></a><span data-ttu-id="ed5a8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed5a8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed5a8-124">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="ed5a8-124">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="ed5a8-125">Puntatore-ereditarietà del tipo di attributo</span><span class="sxs-lookup"><span data-stu-id="ed5a8-125">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[<span data-ttu-id="ed5a8-126">**configurazione di/app \_**</span><span class="sxs-lookup"><span data-stu-id="ed5a8-126">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="ed5a8-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="ed5a8-127">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 