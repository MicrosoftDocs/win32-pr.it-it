---
title: parola chiave sh_file
description: La \_ parola chiave \ sh file \ specifica che l'oggetto di sistema è un handle per un file.
keywords:
- sh_file parola chiave MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f7d2ae0ef4a8166f90700267fa8459525ad4be2f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350966"
---
# <a name="sh_file-keyword"></a><span data-ttu-id="d06fb-104">\_parola chiave file SH</span><span class="sxs-lookup"><span data-stu-id="d06fb-104">sh\_file keyword</span></span>

<span data-ttu-id="d06fb-105">La parola chiave **\_ file SH** specifica che un oggetto `system_handle` include un handle per un file.</span><span class="sxs-lookup"><span data-stu-id="d06fb-105">The **sh\_file** keyword specifies that a `system_handle` holds a handle to a file.</span></span>

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="d06fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d06fb-106">Parameters</span></span>

<span data-ttu-id="d06fb-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="d06fb-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="d06fb-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="d06fb-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="d06fb-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="d06fb-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="d06fb-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d06fb-110">Remarks</span></span>

<span data-ttu-id="d06fb-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="d06fb-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="d06fb-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="d06fb-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
}
```

## <a name="requirements"></a><span data-ttu-id="d06fb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d06fb-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="d06fb-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d06fb-114">Minimum supported client</span></span> | <span data-ttu-id="d06fb-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="d06fb-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="d06fb-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d06fb-116">Minimum supported server</span></span> | <span data-ttu-id="d06fb-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="d06fb-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d06fb-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d06fb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d06fb-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="d06fb-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="d06fb-120">Sicurezza file e diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="d06fb-120">File Security and Access Rights</span></span>](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="d06fb-121">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d06fb-121">DirectComposition</span></span>](/windows/win32/api/_directcomp/)
</dt> <dt>

[<span data-ttu-id="d06fb-122">**DCompositionCreateSurfaceHandle** (funzione)</span><span class="sxs-lookup"><span data-stu-id="d06fb-122">**DCompositionCreateSurfaceHandle** function</span></span>](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
