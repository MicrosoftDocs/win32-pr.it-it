---
title: parola chiave sh_semaphore
description: La \_ parola chiave \ SH Semaphore \ specifica che l'oggetto di sistema è un handle per un semaforo.
keywords:
- sh_semaphore parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2a5c33e4c44b67e3106a48cde244abaf13f41ad5
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "106320233"
---
# <a name="sh_semaphore-keyword"></a><span data-ttu-id="243bb-104">\_parola chiave del semaforo SH</span><span class="sxs-lookup"><span data-stu-id="243bb-104">sh\_semaphore keyword</span></span>

<span data-ttu-id="243bb-105">La parola chiave del **\_ semaforo SH** specifica che un oggetto `system_handle` include un handle per un semaforo.</span><span class="sxs-lookup"><span data-stu-id="243bb-105">The **sh\_semaphore** keyword specifies that a `system_handle` holds a handle to a semaphore.</span></span>

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="243bb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="243bb-106">Parameters</span></span>

<span data-ttu-id="243bb-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="243bb-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="243bb-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="243bb-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="243bb-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="243bb-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="243bb-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="243bb-110">Remarks</span></span>

<span data-ttu-id="243bb-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="243bb-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="243bb-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="243bb-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
}
```

## <a name="requirements"></a><span data-ttu-id="243bb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="243bb-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="243bb-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="243bb-114">Minimum supported client</span></span> | <span data-ttu-id="243bb-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="243bb-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="243bb-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="243bb-116">Minimum supported server</span></span> | <span data-ttu-id="243bb-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="243bb-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="243bb-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="243bb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243bb-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="243bb-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="243bb-120">Oggetti semaforo</span><span class="sxs-lookup"><span data-stu-id="243bb-120">Semaphore Objects</span></span>](../sync/semaphore-objects.md)
</dt> <dt>

[<span data-ttu-id="243bb-121">Sicurezza e diritti di accesso degli oggetti di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="243bb-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="243bb-122">**CreateSemaphore** (funzione)</span><span class="sxs-lookup"><span data-stu-id="243bb-122">**CreateSemaphore** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[<span data-ttu-id="243bb-123">**CreateSemaphoreEx** (funzione)</span><span class="sxs-lookup"><span data-stu-id="243bb-123">**CreateSemaphoreEx** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
