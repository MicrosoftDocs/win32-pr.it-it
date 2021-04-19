---
description: Specifica un elenco delimitato da punti e virgola di server multimediali che possono accettare connessioni da applicazioni client senza usare un server proxy.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: Proprietà MFNETSOURCE_PROXYEXCEPTIONLIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591f7036491964928937f2b48b0656e60f9a20f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311838"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a><span data-ttu-id="8aa1f-103">\_Proprietà PROXYEXCEPTIONLIST di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="8aa1f-103">MFNETSOURCE\_PROXYEXCEPTIONLIST property</span></span>

<span data-ttu-id="8aa1f-104">Specifica un elenco delimitato da punti e virgola di server multimediali che possono accettare connessioni da applicazioni client senza usare un server proxy.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-104">Specifies a semicolon-delimited list of media servers that can accept connections from client applications without using a proxy server.</span></span>



<span data-ttu-id="8aa1f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8aa1f-105">Data type</span></span>

<span data-ttu-id="8aa1f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8aa1f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8aa1f-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8aa1f-107">PROPVARIANT member</span></span>

<span data-ttu-id="8aa1f-108">Stringa di caratteri wide (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="8aa1f-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="8aa1f-109">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="8aa1f-109">VT\_LPWSTR</span></span>

<span data-ttu-id="8aa1f-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="8aa1f-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="8aa1f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8aa1f-111">Remarks</span></span>

<span data-ttu-id="8aa1f-112">La costante **MFNETSOURCE \_ PROXYEXCEPTIONLIST** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-112">The constant **MFNETSOURCE\_PROXYEXCEPTIONLIST** defines the GUID for this property key.</span></span> <span data-ttu-id="8aa1f-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="8aa1f-114">Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="8aa1f-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** nel parametro *PProxyConfig* della funzione [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="8aa1f-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="8aa1f-116">Il localizzatore proxy non esegue il rilevamento del proxy per questi indirizzi.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-116">The proxy locator does not perform proxy detection for these addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa1f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8aa1f-117">Requirements</span></span>



| <span data-ttu-id="8aa1f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aa1f-118">Requirement</span></span> | <span data-ttu-id="8aa1f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8aa1f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa1f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aa1f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa1f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8aa1f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8aa1f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aa1f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa1f-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8aa1f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8aa1f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8aa1f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aa1f-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aa1f-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa1f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8aa1f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa1f-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8aa1f-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8aa1f-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8aa1f-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="8aa1f-129">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="8aa1f-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




