---
title: parola chiave sh_process
description: La \_ parola chiave \ SH Process \ specifica che l'oggetto di sistema è un handle di un processo.
keywords:
- sh_process parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "106320243"
---
# <a name="sh_process-keyword"></a><span data-ttu-id="cb04e-104">\_parola chiave del processo SH</span><span class="sxs-lookup"><span data-stu-id="cb04e-104">sh\_process keyword</span></span>

<span data-ttu-id="cb04e-105">La parola chiave del **\_ processo SH** specifica che un oggetto `system_handle` include un handle per un processo.</span><span class="sxs-lookup"><span data-stu-id="cb04e-105">The **sh\_process** keyword specifies that a `system_handle` holds a handle to a process.</span></span>

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="cb04e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb04e-106">Parameters</span></span>

<span data-ttu-id="cb04e-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="cb04e-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="cb04e-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="cb04e-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="cb04e-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="cb04e-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb04e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb04e-110">Remarks</span></span>

<span data-ttu-id="cb04e-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="cb04e-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="cb04e-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="cb04e-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="cb04e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb04e-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="cb04e-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb04e-114">Minimum supported client</span></span> | <span data-ttu-id="cb04e-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="cb04e-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="cb04e-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb04e-116">Minimum supported server</span></span> | <span data-ttu-id="cb04e-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="cb04e-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="cb04e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb04e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb04e-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="cb04e-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="cb04e-120">Informazioni su processi e thread</span><span class="sxs-lookup"><span data-stu-id="cb04e-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="cb04e-121">Sicurezza del processo e diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="cb04e-121">Process Security and Access Rights</span></span>](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="cb04e-122">**CreateProcess** (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb04e-122">**CreateProcess** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[<span data-ttu-id="cb04e-123">**OpenProcess** (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb04e-123">**OpenProcess** function</span></span>](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>