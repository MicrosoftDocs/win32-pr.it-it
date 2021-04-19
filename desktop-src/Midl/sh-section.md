---
title: parola chiave sh_section
description: La \_ parola chiave \ SH section \ specifica che l'oggetto di sistema è un handle per una sezione.
keywords:
- sh_section parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_section keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 056112deb790e727206a5ac1a1a2a5043a68f5e1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "106320241"
---
# <a name="sh_section-keyword"></a><span data-ttu-id="9fa26-104">\_parola chiave della sezione SH</span><span class="sxs-lookup"><span data-stu-id="9fa26-104">sh\_section keyword</span></span>

<span data-ttu-id="9fa26-105">La parola chiave della **\_ sezione SH** specifica che un oggetto `system_handle` include un handle per una sezione.</span><span class="sxs-lookup"><span data-stu-id="9fa26-105">The **sh\_section** keyword specifies that a `system_handle` holds a handle to a section.</span></span>

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="9fa26-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fa26-106">Parameters</span></span>

<span data-ttu-id="9fa26-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="9fa26-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="9fa26-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="9fa26-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="9fa26-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="9fa26-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fa26-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fa26-110">Remarks</span></span>

<span data-ttu-id="9fa26-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="9fa26-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="9fa26-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="9fa26-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
}
```

## <a name="requirements"></a><span data-ttu-id="9fa26-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fa26-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="9fa26-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fa26-114">Minimum supported client</span></span> | <span data-ttu-id="9fa26-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="9fa26-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="9fa26-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fa26-116">Minimum supported server</span></span> | <span data-ttu-id="9fa26-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="9fa26-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="9fa26-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fa26-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa26-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="9fa26-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="9fa26-120">Oggetti e viste della sezione</span><span class="sxs-lookup"><span data-stu-id="9fa26-120">Section Objects and Views</span></span>](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[<span data-ttu-id="9fa26-121">Funzione **ZwCreateSection** (incluse le specifiche di accesso)</span><span class="sxs-lookup"><span data-stu-id="9fa26-121">**ZwCreateSection** function (including access specifications)</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
