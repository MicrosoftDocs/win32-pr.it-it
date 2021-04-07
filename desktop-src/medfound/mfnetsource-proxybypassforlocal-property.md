---
description: Specifica se il localizzatore proxy deve usare un server proxy per indirizzi locali.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: Proprietà MFNETSOURCE_PROXYBYPASSFORLOCAL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749194"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a><span data-ttu-id="68925-103">\_Proprietà PROXYBYPASSFORLOCAL di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="68925-103">MFNETSOURCE\_PROXYBYPASSFORLOCAL property</span></span>

<span data-ttu-id="68925-104">Specifica se il localizzatore proxy deve usare un server proxy per indirizzi locali.</span><span class="sxs-lookup"><span data-stu-id="68925-104">Specifies whether the proxy locator should use a proxy server for local addresses.</span></span>



<span data-ttu-id="68925-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="68925-105">Data type</span></span>

<span data-ttu-id="68925-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="68925-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="68925-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="68925-107">PROPVARIANT member</span></span>

<span data-ttu-id="68925-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="68925-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="68925-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="68925-109">VT\_I4</span></span>

<span data-ttu-id="68925-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="68925-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="68925-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="68925-111">Remarks</span></span>

<span data-ttu-id="68925-112">La costante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="68925-112">The constant **MFNETSOURCE\_PROXYBYPASSFORLOCAL** defines the GUID for this property key.</span></span> <span data-ttu-id="68925-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="68925-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="68925-114">Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy.</span><span class="sxs-lookup"><span data-stu-id="68925-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="68925-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** nel parametro *PProxyConfig* della funzione [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="68925-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="68925-116">Il valore deve essere impostato su 0 se il server proxy deve essere utilizzato per gli indirizzi locali; in caso contrario, un valore diverso da zero configura il localizzatore proxy predefinito in modo da ignorare il server proxy per gli indirizzi locali.</span><span class="sxs-lookup"><span data-stu-id="68925-116">The value must be set to 0 if the proxy server is to be used for local addresses; otherwise a nonzero value configures the default proxy locator to skip the proxy server for local addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="68925-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68925-117">Requirements</span></span>



| <span data-ttu-id="68925-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="68925-118">Requirement</span></span> | <span data-ttu-id="68925-119">Valore</span><span class="sxs-lookup"><span data-stu-id="68925-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68925-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68925-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68925-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68925-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68925-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68925-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68925-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68925-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68925-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68925-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="68925-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68925-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68925-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68925-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68925-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68925-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="68925-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68925-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="68925-129">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="68925-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




