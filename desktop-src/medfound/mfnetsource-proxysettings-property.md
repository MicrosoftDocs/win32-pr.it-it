---
description: Specifica l'impostazione di configurazione per il localizzatore proxy predefinito.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: Proprietà MFNETSOURCE_PROXYSETTINGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130710"
---
# <a name="mfnetsource_proxysettings-property"></a><span data-ttu-id="3bc1c-103">\_Proprietà PROXYSETTINGS di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="3bc1c-103">MFNETSOURCE\_PROXYSETTINGS property</span></span>

<span data-ttu-id="3bc1c-104">Specifica l'impostazione di configurazione per il localizzatore proxy predefinito.</span><span class="sxs-lookup"><span data-stu-id="3bc1c-104">Specifies the configuration setting for the default proxy locator.</span></span> <span data-ttu-id="3bc1c-105">Il valore di questa proprietà è un membro dell'enumerazione [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) .</span><span class="sxs-lookup"><span data-stu-id="3bc1c-105">The value of this property is a member of the [**MFNET\_PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) enumeration.</span></span>



<span data-ttu-id="3bc1c-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3bc1c-106">Data type</span></span>

<span data-ttu-id="3bc1c-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="3bc1c-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3bc1c-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="3bc1c-108">PROPVARIANT member</span></span>

<span data-ttu-id="3bc1c-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="3bc1c-109">**LONG**</span></span>

<span data-ttu-id="3bc1c-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3bc1c-110">VT\_I4</span></span>

<span data-ttu-id="3bc1c-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="3bc1c-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="3bc1c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bc1c-112">Remarks</span></span>

<span data-ttu-id="3bc1c-113">La costante **MFNETSOURCE \_ PROXYSETTINGS** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="3bc1c-113">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="3bc1c-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="3bc1c-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="3bc1c-115">Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy predefinito.</span><span class="sxs-lookup"><span data-stu-id="3bc1c-115">Applications can use this property to configure the proxy locator when creating the default proxy locator object.</span></span> <span data-ttu-id="3bc1c-116">Per impostare la proprietà, passare un puntatore **IPropertyStore** nel parametro *PProxyConfig* della funzione [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="3bc1c-116">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc1c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bc1c-117">Requirements</span></span>



| <span data-ttu-id="3bc1c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bc1c-118">Requirement</span></span> | <span data-ttu-id="3bc1c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3bc1c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc1c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bc1c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc1c-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3bc1c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3bc1c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bc1c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc1c-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3bc1c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3bc1c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3bc1c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bc1c-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bc1c-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc1c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bc1c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc1c-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3bc1c-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3bc1c-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3bc1c-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="3bc1c-129">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="3bc1c-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




