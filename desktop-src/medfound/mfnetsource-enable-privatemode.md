---
description: Abilita la modalità di download privata nell'origine di rete.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: Proprietà MFNETSOURCE_ENABLE_PRIVATEMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308402"
---
# <a name="mfnetsource_enable_privatemode-property"></a><span data-ttu-id="96af0-103">MFNETSOURCE \_ Abilita \_ Proprietà PRIVATEMODE</span><span class="sxs-lookup"><span data-stu-id="96af0-103">MFNETSOURCE\_ENABLE\_PRIVATEMODE property</span></span>

<span data-ttu-id="96af0-104">Abilita la modalità di download privata nell'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="96af0-104">Enables private download mode in the network source.</span></span>



<span data-ttu-id="96af0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="96af0-105">Data type</span></span>

<span data-ttu-id="96af0-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="96af0-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="96af0-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="96af0-107">PROPVARIANT member</span></span>

<span data-ttu-id="96af0-108">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="96af0-108">**BOOL**</span></span>

<span data-ttu-id="96af0-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="96af0-109">VT\_I4</span></span>

<span data-ttu-id="96af0-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="96af0-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="96af0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="96af0-111">Remarks</span></span>

<span data-ttu-id="96af0-112">Se questa proprietà è **true**, la cache viene cancellata al termine della sessione.</span><span class="sxs-lookup"><span data-stu-id="96af0-112">If this property is **TRUE**, the cache is cleared when the session ends.</span></span>

<span data-ttu-id="96af0-113">La costante **MFNETSOURCE \_ CLIENTGUID** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="96af0-113">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="96af0-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="96af0-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="96af0-115">Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="96af0-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="96af0-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="96af0-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96af0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96af0-117">Requirements</span></span>



| <span data-ttu-id="96af0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="96af0-118">Requirement</span></span> | <span data-ttu-id="96af0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="96af0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96af0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96af0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96af0-121">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="96af0-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="96af0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96af0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96af0-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="96af0-123">None supported</span></span><br/>                                                          |
| <span data-ttu-id="96af0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96af0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="96af0-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96af0-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96af0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96af0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96af0-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96af0-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="96af0-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96af0-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




