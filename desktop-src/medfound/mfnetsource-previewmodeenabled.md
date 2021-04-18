---
description: Abilita o Disabilita la modalità di anteprima, che consente all'applicazione di sovrascrivere la logica di buffer iniziale.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: Proprietà MFNETSOURCE_PREVIEWMODEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315009"
---
# <a name="mfnetsource_previewmodeenabled-property"></a><span data-ttu-id="9e0bf-103">\_Proprietà PREVIEWMODEENABLED di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="9e0bf-103">MFNETSOURCE\_PREVIEWMODEENABLED property</span></span>

<span data-ttu-id="9e0bf-104">Abilita o Disabilita la modalità di anteprima, che consente all'applicazione di sovrascrivere la logica di buffer iniziale.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-104">Enables or disables preview mode, which enables the application to overwrite the initial buffering logic.</span></span>



<span data-ttu-id="9e0bf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9e0bf-105">Data type</span></span>

<span data-ttu-id="9e0bf-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="9e0bf-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9e0bf-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="9e0bf-107">PROPVARIANT member</span></span>

<span data-ttu-id="9e0bf-108">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="9e0bf-108">**BOOL**</span></span>

<span data-ttu-id="9e0bf-109">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="9e0bf-109">VT\_BOOL</span></span>

<span data-ttu-id="9e0bf-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="9e0bf-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="9e0bf-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e0bf-111">Remarks</span></span>

<span data-ttu-id="9e0bf-112">La costante **MFNETSOURCE \_ PREVIEWMODEENABLED** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-112">The constant **MFNETSOURCE\_PREVIEWMODEENABLED** defines the GUID for the property key.</span></span> <span data-ttu-id="9e0bf-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="9e0bf-114">Questa proprietà viene impostata nell'origine di rete passando un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="9e0bf-114">This property is set on the network source by passing an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="9e0bf-115">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="9e0bf-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e0bf-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e0bf-116">Requirements</span></span>



| <span data-ttu-id="9e0bf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e0bf-117">Requirement</span></span> | <span data-ttu-id="9e0bf-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9e0bf-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e0bf-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e0bf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e0bf-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9e0bf-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9e0bf-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e0bf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e0bf-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e0bf-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9e0bf-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e0bf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e0bf-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e0bf-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e0bf-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e0bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e0bf-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e0bf-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9e0bf-127">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e0bf-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




