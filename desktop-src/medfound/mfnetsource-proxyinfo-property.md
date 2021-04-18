---
description: Archivia il nome host e la porta del server proxy utilizzato dall'origine di rete.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: Proprietà MFNETSOURCE_PROXYINFO (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314024"
---
# <a name="mfnetsource_proxyinfo-property"></a><span data-ttu-id="14de5-103">\_Proprietà PROXYINFO di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="14de5-103">MFNETSOURCE\_PROXYINFO property</span></span>

<span data-ttu-id="14de5-104">Archivia il nome host e la porta del server proxy utilizzato dall'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="14de5-104">Stores the host name and the port of the proxy server used by the network source.</span></span>



<span data-ttu-id="14de5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="14de5-105">Data type</span></span>

<span data-ttu-id="14de5-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="14de5-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="14de5-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="14de5-107">PROPVARIANT member</span></span>

<span data-ttu-id="14de5-108">Stringa di caratteri wide (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="14de5-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="14de5-109">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="14de5-109">VT\_LPWSTR</span></span>

<span data-ttu-id="14de5-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="14de5-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="14de5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="14de5-111">Remarks</span></span>

<span data-ttu-id="14de5-112">La costante **MFNETSOURCE \_ PROXYINFO** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="14de5-112">The constant **MFNETSOURCE\_PROXYINFO** defines the GUID for this property key.</span></span> <span data-ttu-id="14de5-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="14de5-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="14de5-114">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="14de5-114">This property is read-only.</span></span> <span data-ttu-id="14de5-115">Per ottenere il valore della proprietà dall'origine di rete, chiamare **IPropertyStore:: GetValue** e passare la struttura **PropertyKey** nel parametro *Key* .</span><span class="sxs-lookup"><span data-stu-id="14de5-115">To get the property value from the network source, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="14de5-116">Il membro **fmtid** di **PropertyKey** deve essere impostato sul GUID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="14de5-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="14de5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14de5-117">Requirements</span></span>



| <span data-ttu-id="14de5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="14de5-118">Requirement</span></span> | <span data-ttu-id="14de5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="14de5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14de5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14de5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14de5-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14de5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="14de5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14de5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14de5-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14de5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="14de5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14de5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="14de5-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14de5-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14de5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14de5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14de5-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14de5-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="14de5-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14de5-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="14de5-129">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="14de5-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




