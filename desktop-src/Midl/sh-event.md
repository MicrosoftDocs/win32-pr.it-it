---
title: parola chiave sh_event
description: La \_ parola chiave \ SH Event \ specifica che l'oggetto di sistema è un handle per un evento.
keywords:
- sh_event parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "106320237"
---
# <a name="sh_event-keyword"></a><span data-ttu-id="ac65d-104">\_parola chiave evento SH</span><span class="sxs-lookup"><span data-stu-id="ac65d-104">sh\_event keyword</span></span>

<span data-ttu-id="ac65d-105">La parola chiave dell' **\_ evento SH** specifica che un oggetto `system_handle` include un handle per un evento.</span><span class="sxs-lookup"><span data-stu-id="ac65d-105">The **sh\_event** keyword specifies that a `system_handle` holds a handle to an event.</span></span>

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="ac65d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac65d-106">Parameters</span></span>

<span data-ttu-id="ac65d-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="ac65d-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="ac65d-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="ac65d-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="ac65d-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="ac65d-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac65d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac65d-110">Remarks</span></span>

<span data-ttu-id="ac65d-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="ac65d-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="ac65d-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="ac65d-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a><span data-ttu-id="ac65d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac65d-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="ac65d-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac65d-114">Minimum supported client</span></span> | <span data-ttu-id="ac65d-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="ac65d-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="ac65d-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac65d-116">Minimum supported server</span></span> | <span data-ttu-id="ac65d-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="ac65d-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ac65d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac65d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac65d-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="ac65d-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="ac65d-120">Oggetti evento</span><span class="sxs-lookup"><span data-stu-id="ac65d-120">Event Objects</span></span>](../sync/event-objects.md)
</dt> <dt>

[<span data-ttu-id="ac65d-121">Sicurezza e diritti di accesso degli oggetti di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="ac65d-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="ac65d-122">**CreateEvent** (funzione)</span><span class="sxs-lookup"><span data-stu-id="ac65d-122">**CreateEvent** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="ac65d-123">**CreateEventEx** (funzione)</span><span class="sxs-lookup"><span data-stu-id="ac65d-123">**CreateEventEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
