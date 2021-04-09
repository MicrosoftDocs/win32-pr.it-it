---
title: Macro di portabilità (RPC. h)
description: Gli strumenti RPC ottengono il modello, la chiamata e l'indipendenza della convenzione di denominazione associando i tipi di dati e i tipi restituiti dalla funzione nei file stub e nei file di intestazione generati con definizioni specifiche per ogni piattaforma.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- RPC macro di portabilità
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "103968835"
---
# <a name="portability-macros"></a><span data-ttu-id="f0195-104">Macro di portabilità</span><span class="sxs-lookup"><span data-stu-id="f0195-104">Portability Macros</span></span>

<span data-ttu-id="f0195-105">Gli strumenti RPC ottengono il modello, la chiamata e l'indipendenza della convenzione di denominazione associando i tipi di dati e i tipi restituiti dalla funzione nei file stub e nei file di intestazione generati con definizioni specifiche per ogni piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f0195-105">The RPC tools achieve model, calling, and naming-convention independence by associating data types and function-return types in the generated stub files and header files with definitions that are specific to each platform.</span></span> <span data-ttu-id="f0195-106">Queste definizioni di macro assicurano che tutti i tipi di dati e le funzioni che richiedono la designazione di **\_ \_ lontano** siano specificati come oggetti lontani.</span><span class="sxs-lookup"><span data-stu-id="f0195-106">These macro definitions ensure that any data types and functions that require the designation of **\_\_far** are specified as far objects.</span></span>

<span data-ttu-id="f0195-107">Nella figura seguente sono illustrate le definizioni di macro che il compilatore MIDL applica alle chiamate di funzione tra i componenti RPC:</span><span class="sxs-lookup"><span data-stu-id="f0195-107">The following figure shows the macro definitions that the MIDL compiler applies to function calls between RPC components:</span></span>

![Diagramma che mostra le definizioni delle macro MIDL si applica alle chiamate di funzione.](images/prog-a29.png)

<span data-ttu-id="f0195-109">Le macro RPC sono definite come segue.</span><span class="sxs-lookup"><span data-stu-id="f0195-109">RPC macros are defined as follows.</span></span>



| <span data-ttu-id="f0195-110">Definizione</span><span class="sxs-lookup"><span data-stu-id="f0195-110">Definition</span></span>    | <span data-ttu-id="f0195-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0195-111">Description</span></span>                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0195-112">\_\_\_API RPC</span><span class="sxs-lookup"><span data-stu-id="f0195-112">\_\_RPC\_API</span></span>  | <span data-ttu-id="f0195-113">Applicato alle chiamate effettuate dallo stub all'applicazione utente.</span><span class="sxs-lookup"><span data-stu-id="f0195-113">Applied to calls made by the stub to the user application.</span></span> <span data-ttu-id="f0195-114">Entrambe le funzioni si trovano nello stesso programma eseguibile.</span><span class="sxs-lookup"><span data-stu-id="f0195-114">Both functions are in the same executable program.</span></span>                                       |
| <span data-ttu-id="f0195-115">\_\_RPC \_ lontano</span><span class="sxs-lookup"><span data-stu-id="f0195-115">\_\_RPC\_FAR</span></span>  | <span data-ttu-id="f0195-116">Applicato alla definizione macro standard per i puntatori.</span><span class="sxs-lookup"><span data-stu-id="f0195-116">Applied to the standard macro definition for pointers.</span></span> <span data-ttu-id="f0195-117">Questa definizione di macro dovrebbe essere inclusa nella firma di tutte le funzioni fornite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f0195-117">This macro definition should appear as part of the signature of all user-supplied functions.</span></span> |
| <span data-ttu-id="f0195-118">\_\_\_Stub RPC</span><span class="sxs-lookup"><span data-stu-id="f0195-118">\_\_RPC\_STUB</span></span> | <span data-ttu-id="f0195-119">Applicato alle chiamate effettuate dalla libreria di Runtime allo stub.</span><span class="sxs-lookup"><span data-stu-id="f0195-119">Applied to calls made from the run-time library to the stub.</span></span> <span data-ttu-id="f0195-120">Queste chiamate possono essere considerate private.</span><span class="sxs-lookup"><span data-stu-id="f0195-120">These calls can be considered private.</span></span>                                                 |
| <span data-ttu-id="f0195-121">\_\_\_utente RPC</span><span class="sxs-lookup"><span data-stu-id="f0195-121">\_\_RPC\_USER</span></span> | <span data-ttu-id="f0195-122">Applicato alle chiamate effettuate dalla libreria di runtime all'applicazione utente.</span><span class="sxs-lookup"><span data-stu-id="f0195-122">Applied to calls made by the run-time library to the user application.</span></span> <span data-ttu-id="f0195-123">Che superano il limite tra una DLL e un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0195-123">These cross the boundary between a DLL and an application.</span></span>                   |
| <span data-ttu-id="f0195-124">\_voce RPC</span><span class="sxs-lookup"><span data-stu-id="f0195-124">RPC\_ENTRY</span></span>    | <span data-ttu-id="f0195-125">Applicato alle chiamate effettuate dall'applicazione o dallo stub alla libreria di Runtime.</span><span class="sxs-lookup"><span data-stu-id="f0195-125">Applied to calls made by the application or stub to the run-time library.</span></span> <span data-ttu-id="f0195-126">Questa definizione di macro viene applicata a tutte le funzioni di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="f0195-126">This macro definition is applied to all RPC run-time functions.</span></span>           |



 

<span data-ttu-id="f0195-127">Per eseguire correttamente il collegamento con le librerie di runtime, gli stub e le routine di supporto di Microsoft RPC, alcune funzioni fornite dall'utente devono includere anche queste macro nella definizione della funzione.</span><span class="sxs-lookup"><span data-stu-id="f0195-127">To link correctly with the Microsoft RPC run-time libraries, stubs, and support routines, some user-supplied functions must also include these macros in the function definition.</span></span> <span data-ttu-id="f0195-128">Utilizzare l' **\_ \_ \_ API RPC** macro quando si definiscono le funzioni associate alla gestione della memoria, gli handle di associazione definiti dall'utente e l'attributo **trasmissione \_ come** e si utilizza l' **\_ \_ \_ utente** della macro RPC quando si definisce la routine di esecuzione del contesto associata all'handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="f0195-128">Use the macro **\_\_RPC\_API** when you define the functions associated with memory management, user-defined binding handles, and the **transmit\_as** attribute, and use the macro **\_\_RPC\_USER** when you define the context run-down routine associated with the context handle.</span></span> <span data-ttu-id="f0195-129">Specificare le funzioni come:</span><span class="sxs-lookup"><span data-stu-id="f0195-129">Specify the functions as:</span></span>

<dl> <dt>

<span data-ttu-id="f0195-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_\_Allocare *utenti \_ MIDL* utente RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="f0195-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC\_USER *midl\_user*\_allocate(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_Utente RPC utente \_ *MIDL \_* \_ gratuito (...)</span><span class="sxs-lookup"><span data-stu-id="f0195-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC\_USER *midl\_user*\_free(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_\_Binding *HANDLETYPE* utente RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="f0195-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC\_USER  *handletype*\_bind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_\_Disassociazione *HANDLETYPE* utente RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="f0195-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC\_USER *handletype*\_unbind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_\_ *Tipo* di utente RPC \_ in \_ locale</span><span class="sxs-lookup"><span data-stu-id="f0195-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC\_USER *type*\_to\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_ *Tipo* di utente RPC \_ da \_ locale</span><span class="sxs-lookup"><span data-stu-id="f0195-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_RPC\_USER *type*\_from\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_Tipo di utente RPC \_ in \_ Xmit (...)</span><span class="sxs-lookup"><span data-stu-id="f0195-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_RPC\_USER type\_to\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_ *Tipo* di utente RPC \_ da \_ Xmit (...)</span><span class="sxs-lookup"><span data-stu-id="f0195-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_RPC\_USER *type*\_from\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_\_ *Tipo* di utente RPC \_ disponibile \_ locale</span><span class="sxs-lookup"><span data-stu-id="f0195-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC\_USER *type*\_free\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_\_ *Tipo* di utente RPC \_ \_ (...)</span><span class="sxs-lookup"><span data-stu-id="f0195-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC\_USER *type*\_free\_inst(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_\_ *Tipo* di utente RPC \_ \_ Xmit gratuito (...)</span><span class="sxs-lookup"><span data-stu-id="f0195-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC\_USER *type*\_free\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f0195-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_\_Rundown del contesto utente RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="f0195-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC\_USER context\_rundown(...)</span></span>
<span data-ttu-id="f0195-142"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f0195-142"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="f0195-143">Tutti i parametri del puntatore in queste funzioni devono essere specificati utilizzando la macro **\_ \_ RPC \_ per** intero.</span><span class="sxs-lookup"><span data-stu-id="f0195-143">All pointer parameters in these functions must be specified using the macro **\_\_RPC\_FAR**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0195-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0195-144">Requirements</span></span>



| <span data-ttu-id="f0195-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0195-145">Requirement</span></span> | <span data-ttu-id="f0195-146">Valore</span><span class="sxs-lookup"><span data-stu-id="f0195-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f0195-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0195-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f0195-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0195-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f0195-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0195-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f0195-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0195-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f0195-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0195-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0195-152"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0195-152"><dt>Rpc.h</dt></span></span> </dl> |



 

 





