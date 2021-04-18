---
description: Specifica la larghezza di banda del collegamento per l'origine di rete, in bit al secondo.
ms.assetid: 1b71dce1-8744-4114-9629-2a9d0afb7c43
title: Proprietà MFNETSOURCE_CONNECTIONBANDWIDTH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b852b3eb8dbfe5d3abc85e2223e868c5be708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527384"
---
# <a name="mfnetsource_connectionbandwidth-property"></a><span data-ttu-id="591b8-103">\_Proprietà CONNECTIONBANDWIDTH di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="591b8-103">MFNETSOURCE\_CONNECTIONBANDWIDTH property</span></span>

<span data-ttu-id="591b8-104">Specifica la larghezza di banda del collegamento per l'origine di rete, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="591b8-104">Specifies the link bandwidth for the network source, in bits per second.</span></span>



<span data-ttu-id="591b8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="591b8-105">Data type</span></span>

<span data-ttu-id="591b8-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="591b8-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="591b8-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="591b8-107">PROPVARIANT member</span></span>

<span data-ttu-id="591b8-108">**DWORD** (archiviato come **Long**)</span><span class="sxs-lookup"><span data-stu-id="591b8-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="591b8-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="591b8-109">VT\_I4</span></span>

<span data-ttu-id="591b8-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="591b8-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="591b8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="591b8-111">Remarks</span></span>

<span data-ttu-id="591b8-112">La costante **MFNETSOURCE \_ CONNECTIONBANDWIDTH** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="591b8-112">The constant **MFNETSOURCE\_CONNECTIONBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="591b8-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="591b8-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="591b8-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="591b8-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="591b8-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="591b8-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="591b8-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="591b8-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="591b8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="591b8-117">Requirements</span></span>



| <span data-ttu-id="591b8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="591b8-118">Requirement</span></span> | <span data-ttu-id="591b8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="591b8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="591b8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="591b8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="591b8-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="591b8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="591b8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="591b8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="591b8-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="591b8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="591b8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="591b8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="591b8-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="591b8-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="591b8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="591b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="591b8-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="591b8-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="591b8-128">Funzionalità di origine della rete</span><span class="sxs-lookup"><span data-stu-id="591b8-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="591b8-129">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="591b8-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




