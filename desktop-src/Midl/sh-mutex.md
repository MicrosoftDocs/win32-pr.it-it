---
title: parola chiave sh_mutex
description: La \_ parola chiave \ SH mutex \ specifica che l'oggetto di sistema è un handle per un mutex.
keywords:
- sh_mutex parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321026"
---
# <a name="sh_mutex-keyword"></a><span data-ttu-id="ee1cb-104">SH \_ mutex (parola chiave)</span><span class="sxs-lookup"><span data-stu-id="ee1cb-104">sh\_mutex keyword</span></span>

<span data-ttu-id="ee1cb-105">La parola chiave del **\_ mutex SH** specifica che un oggetto `system_handle` include un handle per un mutex.</span><span class="sxs-lookup"><span data-stu-id="ee1cb-105">The **sh\_mutex** keyword specifies that a `system_handle` holds a handle to a mutex.</span></span>

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="ee1cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee1cb-106">Parameters</span></span>

<span data-ttu-id="ee1cb-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="ee1cb-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="ee1cb-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="ee1cb-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="ee1cb-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="ee1cb-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee1cb-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee1cb-110">Remarks</span></span>

<span data-ttu-id="ee1cb-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="ee1cb-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="ee1cb-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="ee1cb-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
}
```

## <a name="requirements"></a><span data-ttu-id="ee1cb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee1cb-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="ee1cb-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee1cb-114">Minimum supported client</span></span> | <span data-ttu-id="ee1cb-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="ee1cb-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="ee1cb-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee1cb-116">Minimum supported server</span></span> | <span data-ttu-id="ee1cb-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="ee1cb-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ee1cb-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee1cb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1cb-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="ee1cb-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="ee1cb-120">Oggetti mutex</span><span class="sxs-lookup"><span data-stu-id="ee1cb-120">Mutex Objects</span></span>](../sync/mutex-objects.md)
</dt> <dt>

[<span data-ttu-id="ee1cb-121">Sicurezza e diritti di accesso degli oggetti di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="ee1cb-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="ee1cb-122">**CreateMutex** (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee1cb-122">**CreateMutex** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[<span data-ttu-id="ee1cb-123">**CreateMutexEx** (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee1cb-123">**CreateMutexEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>