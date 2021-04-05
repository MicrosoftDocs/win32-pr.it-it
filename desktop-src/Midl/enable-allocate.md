---
title: attributo enable_allocate
description: L'attributo \ enable \_ allocate \ ACF specifica che il codice stub del server deve abilitare l'ambiente di gestione della memoria stub.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- attributo enable_allocate MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117615"
---
# <a name="enable_allocate-attribute"></a><span data-ttu-id="5f983-104">Abilita \_ attributo allocate</span><span class="sxs-lookup"><span data-stu-id="5f983-104">enable\_allocate attribute</span></span>

<span data-ttu-id="5f983-105">L'attributo **\[ enable \_ allocate \]** ACF specifica che il codice stub del server deve abilitare l'ambiente di gestione della memoria stub.</span><span class="sxs-lookup"><span data-stu-id="5f983-105">The **\[enable\_allocate\]** ACF attribute specifies that the server stub code should enable the stub memory management environment.</span></span>

> [!Note]  
> <span data-ttu-id="5f983-106">L'attributo **\[ enable \_ allocate \]** è obsoleto e non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="5f983-106">The **\[enable\_allocate\]** attribute is obsolete and is no longer supported.</span></span>

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="5f983-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f983-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f983-108">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5f983-108">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5f983-109">Specifica un elenco di zero o più attributi MIDL aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5f983-109">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="5f983-110">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="5f983-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5f983-111">Nome dell'interfaccia a cui verrà applicato l'attributo **\[ enable \_ allcoate \]** .</span><span class="sxs-lookup"><span data-stu-id="5f983-111">The name of the interface to which the **\[enable\_allcoate\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f983-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f983-112">Remarks</span></span>

<span data-ttu-id="5f983-113">In modalità predefinita, lo stub del server Abilita l'ambiente di memoria solo quando viene usato l'attributo **\[ enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="5f983-113">In default mode, the server stub enables the memory environment only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="5f983-114">Per poter allocare memoria tramite [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate), è necessario abilitare l'ambiente di gestione della memoria.</span><span class="sxs-lookup"><span data-stu-id="5f983-114">The memory management environment must be enabled before memory can be allocated using [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span></span> <span data-ttu-id="5f983-115">In modalità **OSF** (quando si esegue la compilazione con l'opzione [**/OSF**](-osf.md) ), lo stub Abilita automaticamente questo ambiente o su richiesta quando viene usato l'attributo **\[ enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="5f983-115">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the stub enables this environment automatically, or on request when the **\[enable\_allocate\]** attribute is used.</span></span>

<span data-ttu-id="5f983-116">Lo stub lato client può essere sensibile all'ambiente di gestione della memoria **RPCSS** .</span><span class="sxs-lookup"><span data-stu-id="5f983-116">The client side stub may be sensitive to the **Rpcss** memory management environment.</span></span> <span data-ttu-id="5f983-117">Se viene eseguito uno stub client sensibile quando il pacchetto **RPCSS** è disabilitato, vengono chiamati gli allocatori/deallocatori utente predefiniti, ad esempio [MIDL \_ User \_ Alloch](/windows/desktop/Rpc/the-midl-user-allocate-function) /  [MIDL \_ User \_ Free](/windows/desktop/Rpc/the-midl-user-free-function).</span><span class="sxs-lookup"><span data-stu-id="5f983-117">If a sensitive client stub is executed when the **Rpcss** package is disabled, the default user allocator/deallocators are called (for example, [midl\_user\_allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)/ [midl\_user\_free](/windows/desktop/Rpc/the-midl-user-free-function)).</span></span> <span data-ttu-id="5f983-118">Se abilitata, il pacchetto **RPCSS** utilizza la coppia allocatore/deallocatore del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5f983-118">When enabled, the **Rpcss** package uses the allocator/deallocator pair from the package.</span></span> <span data-ttu-id="5f983-119">Nella modalità predefinita, il client è sensibile solo quando viene utilizzato l'attributo **\[ enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="5f983-119">In the default mode, the client is sensitive only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="5f983-120">In genere, lo stub lato client opera nell'ambiente disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5f983-120">Typically, the client side stub operates in the disabled environment.</span></span> <span data-ttu-id="5f983-121">In modalità **OSF** (quando si esegue la compilazione con l'opzione [**/OSF**](-osf.md) ), il client è sempre sensibile all'ambiente di gestione della memoria **RPCSS** e, di conseguenza, l'attributo **\[ enable \_ allocate \]** non influirà sugli stub client.</span><span class="sxs-lookup"><span data-stu-id="5f983-121">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the client is always sensitive to the **Rpcss** memory management environment and, therefore, the **\[enable\_allocate\]** attribute will not affect the client stubs.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f983-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f983-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f983-123">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="5f983-123">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="5f983-124">\_alloca utente \_ MIDL</span><span class="sxs-lookup"><span data-stu-id="5f983-124">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="5f983-125">\_utente MIDL \_ gratuito</span><span class="sxs-lookup"><span data-stu-id="5f983-125">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="5f983-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="5f983-126">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="5f983-127">RpcSmDisableAllocate</span><span class="sxs-lookup"><span data-stu-id="5f983-127">RpcSmDisableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[<span data-ttu-id="5f983-128">RpcSmEnableAllocate</span><span class="sxs-lookup"><span data-stu-id="5f983-128">RpcSmEnableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[<span data-ttu-id="5f983-129">RpcSmFree</span><span class="sxs-lookup"><span data-stu-id="5f983-129">RpcSmFree</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 