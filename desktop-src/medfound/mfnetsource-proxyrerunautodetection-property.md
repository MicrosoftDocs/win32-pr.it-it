---
description: Specifica se il localizzatore proxy predefinito deve forzare il rilevamento automatico del proxy.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: Proprietà MFNETSOURCE_PROXYRERUNAUTODETECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528225"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a><span data-ttu-id="b8488-103">\_Proprietà PROXYRERUNAUTODETECTION di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="b8488-103">MFNETSOURCE\_PROXYRERUNAUTODETECTION property</span></span>

<span data-ttu-id="b8488-104">Specifica se il localizzatore proxy predefinito deve forzare il rilevamento automatico del proxy.</span><span class="sxs-lookup"><span data-stu-id="b8488-104">Specifies whether the default proxy locator should force proxy auto-detection.</span></span>



<span data-ttu-id="b8488-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b8488-105">Data type</span></span>

<span data-ttu-id="b8488-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="b8488-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b8488-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="b8488-107">PROPVARIANT member</span></span>

<span data-ttu-id="b8488-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="b8488-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="b8488-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b8488-109">VT\_I4</span></span>

<span data-ttu-id="b8488-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="b8488-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="b8488-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8488-111">Remarks</span></span>

<span data-ttu-id="b8488-112">La costante **MFNETSOURCE \_ PROXYSETTINGS** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b8488-112">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="b8488-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="b8488-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="b8488-114">Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy.</span><span class="sxs-lookup"><span data-stu-id="b8488-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="b8488-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** nel parametro *PProxyConfig* della funzione [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="b8488-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="b8488-116">Nella modalità di rilevamento automatico, il localizzatore proxy usa il meccanismo di rilevamento del proxy WinInet.</span><span class="sxs-lookup"><span data-stu-id="b8488-116">In auto-detect mode, the proxy locator uses the WinInet proxy detection mechanism.</span></span> <span data-ttu-id="b8488-117">Per forzare il rilevamento automatico, impostare il valore su 0.</span><span class="sxs-lookup"><span data-stu-id="b8488-117">To force auto-detection, set the value to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8488-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8488-118">Requirements</span></span>



| <span data-ttu-id="b8488-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8488-119">Requirement</span></span> | <span data-ttu-id="b8488-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b8488-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8488-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8488-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b8488-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8488-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b8488-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8488-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b8488-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8488-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b8488-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8488-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8488-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8488-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8488-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8488-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8488-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8488-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b8488-129">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8488-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="b8488-130">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="b8488-130">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




