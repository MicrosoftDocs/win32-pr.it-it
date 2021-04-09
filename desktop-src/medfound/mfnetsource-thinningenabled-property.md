---
description: Specifica se il cambio di flusso è abilitato nell'origine di rete.
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: Proprietà MFNETSOURCE_THINNINGENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d5b1b362f8776e80e3d12b591dbf2116217846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966399"
---
# <a name="mfnetsource_thinningenabled-property"></a><span data-ttu-id="33a05-103">\_Proprietà THINNINGENABLED di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="33a05-103">MFNETSOURCE\_THINNINGENABLED property</span></span>

<span data-ttu-id="33a05-104">Specifica se il cambio di flusso è abilitato nell'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="33a05-104">Specifies whether stream switching is enabled on the network source.</span></span> <span data-ttu-id="33a05-105">Il cambio di flusso consente al server multimediale di modificare i flussi in un file con più velocità in bit (MBR), in base alla larghezza di banda disponibile.</span><span class="sxs-lookup"><span data-stu-id="33a05-105">Stream switching enables the media server to change streams in a multiple bit-rate (MBR) file, based on available bandwidth.</span></span>



<span data-ttu-id="33a05-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="33a05-106">Data type</span></span>

<span data-ttu-id="33a05-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="33a05-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="33a05-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="33a05-108">PROPVARIANT member</span></span>

<span data-ttu-id="33a05-109">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="33a05-109">Boolean (**LONG**)</span></span>

<span data-ttu-id="33a05-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="33a05-110">VT\_I4</span></span>

<span data-ttu-id="33a05-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="33a05-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="33a05-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="33a05-112">Remarks</span></span>

<span data-ttu-id="33a05-113">La costante **MFNETSOURCE \_ THINNINGENABLED** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="33a05-113">The constant **MFNETSOURCE\_THINNINGENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="33a05-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="33a05-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="33a05-115">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="33a05-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="33a05-116">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="33a05-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="33a05-117">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="33a05-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="33a05-118">Il valore predefinito di questa proprietà è **true**.</span><span class="sxs-lookup"><span data-stu-id="33a05-118">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a05-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33a05-119">Requirements</span></span>



| <span data-ttu-id="33a05-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="33a05-120">Requirement</span></span> | <span data-ttu-id="33a05-121">Valore</span><span class="sxs-lookup"><span data-stu-id="33a05-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33a05-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33a05-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33a05-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33a05-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="33a05-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33a05-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33a05-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33a05-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="33a05-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33a05-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="33a05-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="33a05-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a05-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33a05-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a05-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33a05-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="33a05-130">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33a05-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




