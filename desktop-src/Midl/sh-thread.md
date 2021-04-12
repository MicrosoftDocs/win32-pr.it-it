---
title: parola chiave sh_thread
description: La \_ parola chiave \ SH thread \ specifica che l'oggetto di sistema è un handle per un thread.
keywords:
- sh_thread parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2c82dc41d2b1c7cba740c897ef6cea9094979cc3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104234427"
---
# <a name="sh_thread-keyword"></a><span data-ttu-id="8c513-104">\_parola chiave del thread SH</span><span class="sxs-lookup"><span data-stu-id="8c513-104">sh\_thread keyword</span></span>

<span data-ttu-id="8c513-105">La parola chiave del **\_ thread SH** specifica che un oggetto `system_handle` include un handle per un thread.</span><span class="sxs-lookup"><span data-stu-id="8c513-105">The **sh\_thread** keyword specifies that a `system_handle` holds a handle to a thread.</span></span>

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="8c513-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c513-106">Parameters</span></span>

<span data-ttu-id="8c513-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="8c513-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="8c513-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="8c513-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="8c513-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="8c513-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c513-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c513-110">Remarks</span></span>

<span data-ttu-id="8c513-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="8c513-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="8c513-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="8c513-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="8c513-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c513-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="8c513-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c513-114">Minimum supported client</span></span> | <span data-ttu-id="8c513-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="8c513-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="8c513-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c513-116">Minimum supported server</span></span> | <span data-ttu-id="8c513-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="8c513-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="8c513-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c513-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c513-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="8c513-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="8c513-120">Informazioni su processi e thread</span><span class="sxs-lookup"><span data-stu-id="8c513-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="8c513-121">Sicurezza dei thread e diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="8c513-121">Thread Security and Access Rights</span></span>](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="8c513-122">**CreateThread** (funzione)</span><span class="sxs-lookup"><span data-stu-id="8c513-122">**CreateThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[<span data-ttu-id="8c513-123">**OpenThread** (funzione)</span><span class="sxs-lookup"><span data-stu-id="8c513-123">**OpenThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>