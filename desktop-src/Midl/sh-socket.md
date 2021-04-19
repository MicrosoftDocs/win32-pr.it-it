---
title: parola chiave sh_socket
description: La \_ parola chiave \ SH socket \ specifica che l'oggetto di sistema è un handle per un socket.
keywords:
- sh_socket parola chiave MIDL
topic_type:
- apiref
api_name:
- sh_socket keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5f5d2506f66f89cd47ecf3f011c8071b79e64177
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "106320240"
---
# <a name="sh_socket-keyword"></a><span data-ttu-id="bda5b-104">\_parola chiave socket SH</span><span class="sxs-lookup"><span data-stu-id="bda5b-104">sh\_socket keyword</span></span>

<span data-ttu-id="bda5b-105">La parola chiave **\_ socket SH** specifica che un oggetto `system_handle` include un handle per un socket.</span><span class="sxs-lookup"><span data-stu-id="bda5b-105">The **sh\_socket** keyword specifies that a `system_handle` holds a handle to a socket.</span></span>

``` syntax
[system_handle(sh_socket)]

[system_handle(sh_socket, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="bda5b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bda5b-106">Parameters</span></span>

<span data-ttu-id="bda5b-107">Questa parola chiave è un parametro per [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="bda5b-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="bda5b-108">La documentazione di [**system_handle**](system-handle.md) contiene inoltre informazioni dettagliate sull'utilizzo facoltativo del parametro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="bda5b-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="bda5b-109">Il comportamento predefinito è `DUPLICATE_SAME_ACCESS` per le specifiche della [funzione **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="bda5b-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="bda5b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="bda5b-110">Remarks</span></span>

<span data-ttu-id="bda5b-111">Per usare questa parola chiave con l' `system_handle` attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.</span><span class="sxs-lookup"><span data-stu-id="bda5b-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="bda5b-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="bda5b-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT ListenToSocket([in, system_handle(sh_socket)] HANDLE socket);
}
```

## <a name="requirements"></a><span data-ttu-id="bda5b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bda5b-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="bda5b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda5b-114">Minimum supported client</span></span> | <span data-ttu-id="bda5b-115">Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="bda5b-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="bda5b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda5b-116">Minimum supported server</span></span> | <span data-ttu-id="bda5b-117">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="bda5b-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="bda5b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bda5b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda5b-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="bda5b-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="bda5b-120">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="bda5b-120">Windows Sockets 2</span></span>](../winsock/windows-sockets-start-page-2.md)
</dt> </dl>
