---
description: Specifica se sono abilitati tutti i protocolli di download.
ms.assetid: c178693f-44ea-481e-b7f2-2ec94eea1994
title: Proprietà MFNETSOURCE_ENABLE_DOWNLOAD (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1b57d8ab984f7c198d1c1b43455f2d0d5dda68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049607"
---
# <a name="mfnetsource_enable_download-property"></a><span data-ttu-id="2c03b-103">\_Proprietà Abilita \_ download di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="2c03b-103">MFNETSOURCE\_ENABLE\_DOWNLOAD property</span></span>

<span data-ttu-id="2c03b-104">Specifica se sono abilitati tutti i protocolli di download.</span><span class="sxs-lookup"><span data-stu-id="2c03b-104">Specifies whether all download protocols are enabled.</span></span>



<span data-ttu-id="2c03b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2c03b-105">Data type</span></span>

<span data-ttu-id="2c03b-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="2c03b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2c03b-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="2c03b-107">PROPVARIANT member</span></span>

<span data-ttu-id="2c03b-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="2c03b-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="2c03b-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2c03b-109">VT\_I4</span></span>

<span data-ttu-id="2c03b-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="2c03b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2c03b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c03b-111">Remarks</span></span>

<span data-ttu-id="2c03b-112">La costante **MFNETSOURCE \_ enable \_ download** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="2c03b-112">The constant **MFNETSOURCE\_ENABLE\_DOWNLOAD** defines the GUID for this property key.</span></span> <span data-ttu-id="2c03b-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="2c03b-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="2c03b-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="2c03b-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="2c03b-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** alla [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2c03b-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c03b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c03b-116">Requirements</span></span>



| <span data-ttu-id="2c03b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c03b-117">Requirement</span></span> | <span data-ttu-id="2c03b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2c03b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c03b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c03b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c03b-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c03b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2c03b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c03b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c03b-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c03b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2c03b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c03b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c03b-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c03b-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c03b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c03b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c03b-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c03b-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2c03b-127">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c03b-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="2c03b-128">Protocolli supportati</span><span class="sxs-lookup"><span data-stu-id="2c03b-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




