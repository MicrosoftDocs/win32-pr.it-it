---
description: Il numero di volte che l'origine di rete ha tentato di riconnettersi alla rete.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: Proprietà MFNETSOURCE_AUTORECONNECTPROGRESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308408"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a><span data-ttu-id="306b9-103">\_Proprietà AUTORECONNECTPROGRESS di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="306b9-103">MFNETSOURCE\_AUTORECONNECTPROGRESS property</span></span>

<span data-ttu-id="306b9-104">Il numero di volte che l'origine di rete ha tentato di riconnettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="306b9-104">The number of times the network source has attempted to reconnect to the network.</span></span>



<span data-ttu-id="306b9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="306b9-105">Data type</span></span>

<span data-ttu-id="306b9-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="306b9-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="306b9-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="306b9-107">PROPVARIANT member</span></span>

<span data-ttu-id="306b9-108">**DWORD** (archiviato come **Long**)</span><span class="sxs-lookup"><span data-stu-id="306b9-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="306b9-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="306b9-109">VT\_I4</span></span>

<span data-ttu-id="306b9-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="306b9-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="306b9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="306b9-111">Remarks</span></span>

<span data-ttu-id="306b9-112">La costante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="306b9-112">The constant **MFNETSOURCE\_AUTORECONNECTPROGRESS** defines the GUID for this property key.</span></span> <span data-ttu-id="306b9-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="306b9-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="306b9-114">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="306b9-114">This property is read-only.</span></span> <span data-ttu-id="306b9-115">Per recuperare questa proprietà, eseguire una query sull'origine di rete per l'interfaccia **IPropertyStore** e chiamare **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="306b9-115">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="306b9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="306b9-116">Requirements</span></span>



| <span data-ttu-id="306b9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="306b9-117">Requirement</span></span> | <span data-ttu-id="306b9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="306b9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="306b9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="306b9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="306b9-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="306b9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="306b9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="306b9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="306b9-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="306b9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="306b9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="306b9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="306b9-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="306b9-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="306b9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="306b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="306b9-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="306b9-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="306b9-127">Funzionalità di origine della rete</span><span class="sxs-lookup"><span data-stu-id="306b9-127">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="306b9-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="306b9-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




