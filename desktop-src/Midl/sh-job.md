---
title: parola chiave sh_job
description: La \_ parola chiave \ SH Job \ specifica che l'oggetto di sistema è un handle di un processo.
keywords:
- sh_job parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: db24f9dc84f2bb56f57327090485b406ad1a437f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "103968813"
---
# <a name="sh_job-keyword"></a><span data-ttu-id="5deb1-104">\_parola chiave del processo SH</span><span class="sxs-lookup"><span data-stu-id="5deb1-104">sh\_job keyword</span></span>

<span data-ttu-id="5deb1-105">La parola chiave del **\_ processo SH** specifica che un oggetto `system_handle` include un handle per un processo.</span><span class="sxs-lookup"><span data-stu-id="5deb1-105">The **sh\_job** keyword specifies that a `system_handle` holds a handle to a job.</span></span>

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="5deb1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5deb1-106">Parameters</span></span>

<span data-ttu-id="5deb1-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="5deb1-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="5deb1-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="5deb1-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="5deb1-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="5deb1-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="5deb1-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5deb1-110">Remarks</span></span>

<span data-ttu-id="5deb1-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="5deb1-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="5deb1-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="5deb1-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
}
```

## <a name="requirements"></a><span data-ttu-id="5deb1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5deb1-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="5deb1-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5deb1-114">Minimum supported client</span></span> | <span data-ttu-id="5deb1-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="5deb1-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="5deb1-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5deb1-116">Minimum supported server</span></span> | <span data-ttu-id="5deb1-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="5deb1-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5deb1-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5deb1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5deb1-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="5deb1-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="5deb1-120">Oggetti processo</span><span class="sxs-lookup"><span data-stu-id="5deb1-120">Job Objects</span></span>](../procthread/job-objects.md)
</dt> <dt>

[<span data-ttu-id="5deb1-121">Sicurezza dell'oggetto processo e diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="5deb1-121">Job Object Security and Access Rights</span></span>](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="5deb1-122">**CreateJobObject** (funzione)</span><span class="sxs-lookup"><span data-stu-id="5deb1-122">**CreateJobObject** function</span></span>](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
