---
title: parola chiave sh_composition
description: La \_ parola chiave \ SH Composition \ specifica che l'oggetto di sistema è un handle per una superficie di composizione.
keywords:
- sh_composition parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_composition
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5a7e723c65ca6320dbec4a2f8a379cfed2f85f72
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104234422"
---
# <a name="sh_composition-keyword"></a><span data-ttu-id="59b00-104">\_parola chiave di composizione SH</span><span class="sxs-lookup"><span data-stu-id="59b00-104">sh\_composition keyword</span></span>

<span data-ttu-id="59b00-105">La parola chiave di **\_ composizione SH** specifica che un oggetto `system_handle` include un handle per una superficie di composizione.</span><span class="sxs-lookup"><span data-stu-id="59b00-105">The **sh\_composition** keyword specifies that a `system_handle` holds a handle to a composition surface.</span></span>

``` syntax
[system_handle(sh_composition)]

[system_handle(sh_composition, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="59b00-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59b00-106">Parameters</span></span>

<span data-ttu-id="59b00-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="59b00-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="59b00-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="59b00-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="59b00-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="59b00-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="59b00-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="59b00-110">Remarks</span></span>

<span data-ttu-id="59b00-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="59b00-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="59b00-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="59b00-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetVisualSurface([out, system_handle(sh_composition)] HANDLE* visual);
}
```

## <a name="requirements"></a><span data-ttu-id="59b00-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59b00-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="59b00-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59b00-114">Minimum supported client</span></span> | <span data-ttu-id="59b00-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="59b00-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="59b00-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59b00-116">Minimum supported server</span></span> | <span data-ttu-id="59b00-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="59b00-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="59b00-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59b00-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b00-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="59b00-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="59b00-120">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="59b00-120">DirectComposition</span></span>](/windows/win32/api/_directcomp/)
</dt> <dt>

[<span data-ttu-id="59b00-121">**DCompositionCreateSurfaceHandle** (funzione)</span><span class="sxs-lookup"><span data-stu-id="59b00-121">**DCompositionCreateSurfaceHandle** function</span></span>](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> </dl>
