---
description: Specifica il numero di porta del server proxy.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: Proprietà MFNETSOURCE_PROXYPORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226628"
---
# <a name="mfnetsource_proxyport-property"></a><span data-ttu-id="3d067-103">\_Proprietà PROXYPORT di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="3d067-103">MFNETSOURCE\_PROXYPORT property</span></span>

<span data-ttu-id="3d067-104">Specifica il numero di porta del server proxy.</span><span class="sxs-lookup"><span data-stu-id="3d067-104">Specifies the port number of the proxy server.</span></span>



<span data-ttu-id="3d067-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3d067-105">Data type</span></span>

<span data-ttu-id="3d067-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="3d067-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3d067-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="3d067-107">PROPVARIANT member</span></span>

<span data-ttu-id="3d067-108">**DWORD** (archiviato come **Long**)</span><span class="sxs-lookup"><span data-stu-id="3d067-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="3d067-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3d067-109">VT\_I4</span></span>

<span data-ttu-id="3d067-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="3d067-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="3d067-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d067-111">Remarks</span></span>

<span data-ttu-id="3d067-112">La costante **MFNETSOURCE \_ PROXYPORT** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="3d067-112">The constant **MFNETSOURCE\_PROXYPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="3d067-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="3d067-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="3d067-114">Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy.</span><span class="sxs-lookup"><span data-stu-id="3d067-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="3d067-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** nel parametro *PProxyConfig* della funzione [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="3d067-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="3d067-116">Se questa proprietà non è impostata per HTTP, per impostazione predefinita il localizzatore proxy usa un valore di 80.</span><span class="sxs-lookup"><span data-stu-id="3d067-116">If this property is not set for HTTP, then by default the proxy locator uses a value of 80.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d067-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d067-117">Requirements</span></span>



| <span data-ttu-id="3d067-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d067-118">Requirement</span></span> | <span data-ttu-id="3d067-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3d067-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d067-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d067-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d067-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d067-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d067-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d067-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d067-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3d067-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3d067-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d067-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d067-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d067-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d067-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d067-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d067-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d067-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3d067-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d067-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="3d067-129">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="3d067-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




