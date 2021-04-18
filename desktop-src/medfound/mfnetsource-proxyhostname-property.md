---
description: Specifica il nome host del server proxy.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: Proprietà MFNETSOURCE_PROXYHOSTNAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc59d5b827276eb5063febf7a8cb7647002ca72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307959"
---
# <a name="mfnetsource_proxyhostname-property"></a><span data-ttu-id="4227f-103">\_Proprietà PROXYHOSTNAME di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="4227f-103">MFNETSOURCE\_PROXYHOSTNAME property</span></span>

<span data-ttu-id="4227f-104">Specifica il nome host del server proxy.</span><span class="sxs-lookup"><span data-stu-id="4227f-104">Specifies the host name of the proxy server.</span></span>



<span data-ttu-id="4227f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4227f-105">Data type</span></span>

<span data-ttu-id="4227f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="4227f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4227f-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="4227f-107">PROPVARIANT member</span></span>

<span data-ttu-id="4227f-108">Stringa di caratteri wide (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="4227f-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="4227f-109">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="4227f-109">VT\_LPWSTR</span></span>

<span data-ttu-id="4227f-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="4227f-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="4227f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4227f-111">Remarks</span></span>

<span data-ttu-id="4227f-112">La costante **MFNETSOURCE \_ PROXYHOSTNAME** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="4227f-112">The constant **MFNETSOURCE\_PROXYHOSTNAME** defines the GUID for this property key.</span></span> <span data-ttu-id="4227f-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="4227f-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="4227f-114">Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy predefinito durante la creazione dell'oggetto localizzatore proxy.</span><span class="sxs-lookup"><span data-stu-id="4227f-114">Applications can use this property to configure the default proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="4227f-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** nel parametro *PProxyConfig* della funzione [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="4227f-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="4227f-116">Questa proprietà deve essere impostata dall'applicazione quando il localizzatore proxy è configurato per operare in modalità manuale.</span><span class="sxs-lookup"><span data-stu-id="4227f-116">This property must be set by the application when the proxy locator is configured to operate in the manual mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="4227f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4227f-117">Requirements</span></span>



| <span data-ttu-id="4227f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4227f-118">Requirement</span></span> | <span data-ttu-id="4227f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4227f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4227f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4227f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4227f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4227f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4227f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4227f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4227f-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4227f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4227f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4227f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4227f-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4227f-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4227f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4227f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4227f-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4227f-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4227f-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4227f-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="4227f-129">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="4227f-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




