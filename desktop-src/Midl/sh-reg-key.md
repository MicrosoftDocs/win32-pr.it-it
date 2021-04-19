---
title: parola chiave sh_reg_key
description: La parola chiave \ sh \_ reg \_ Key \ specifica che l'oggetto di sistema è un handle per una chiave del registro di sistema.
keywords:
- sh_reg_key parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "106320242"
---
# <a name="sh_reg_key-keyword"></a><span data-ttu-id="7dc7f-104">\_ \_ parola chiave del codice SH reg</span><span class="sxs-lookup"><span data-stu-id="7dc7f-104">sh\_reg\_key keyword</span></span>

<span data-ttu-id="7dc7f-105">La parola chiave del **\_ \_ codice SH reg** specifica che un oggetto `system_handle` include un handle per una chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7dc7f-105">The **sh\_reg\_key** keyword specifies that a `system_handle` holds a handle to a registry key.</span></span>

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="7dc7f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7dc7f-106">Parameters</span></span>

<span data-ttu-id="7dc7f-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="7dc7f-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="7dc7f-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="7dc7f-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="7dc7f-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="7dc7f-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc7f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7dc7f-110">Remarks</span></span>

<span data-ttu-id="7dc7f-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="7dc7f-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="7dc7f-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="7dc7f-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
}
```

## <a name="requirements"></a><span data-ttu-id="7dc7f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dc7f-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="7dc7f-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dc7f-114">Minimum supported client</span></span> | <span data-ttu-id="7dc7f-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="7dc7f-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="7dc7f-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dc7f-116">Minimum supported server</span></span> | <span data-ttu-id="7dc7f-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="7dc7f-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="7dc7f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7dc7f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc7f-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="7dc7f-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="7dc7f-120">Registro</span><span class="sxs-lookup"><span data-stu-id="7dc7f-120">Registry</span></span>](../sysinfo/registry.md)
</dt> <dt>

[<span data-ttu-id="7dc7f-121">Diritti di accesso e sicurezza della chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="7dc7f-121">Registry Key Security and Access Rights</span></span>](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="7dc7f-122">**RegOpenKeyEx** (funzione)</span><span class="sxs-lookup"><span data-stu-id="7dc7f-122">**RegOpenKeyEx** function</span></span>](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
