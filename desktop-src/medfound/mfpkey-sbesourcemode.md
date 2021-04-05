---
description: Imposta la configurazione di flusso per l'origine del supporto WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: Proprietà MFPKEY_SBESourceMode (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967164"
---
# <a name="mfpkey_sbesourcemode-property"></a><span data-ttu-id="6fa5c-103">\_Proprietà SBESourceMode di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="6fa5c-103">MFPKEY\_SBESourceMode property</span></span>

<span data-ttu-id="6fa5c-104">Imposta la configurazione di flusso per l'origine del supporto WTV.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-104">Sets the stream configuration for the WTV media source.</span></span>



<span data-ttu-id="6fa5c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6fa5c-105">Data type</span></span>

<span data-ttu-id="6fa5c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="6fa5c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6fa5c-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="6fa5c-107">PROPVARIANT member</span></span>

<span data-ttu-id="6fa5c-108">**INT**</span><span class="sxs-lookup"><span data-stu-id="6fa5c-108">**INT**</span></span>

<span data-ttu-id="6fa5c-109">\_int VT</span><span class="sxs-lookup"><span data-stu-id="6fa5c-109">VT\_INT</span></span>

<span data-ttu-id="6fa5c-110">**intVal**</span><span class="sxs-lookup"><span data-stu-id="6fa5c-110">**intVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6fa5c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fa5c-111">Remarks</span></span>

<span data-ttu-id="6fa5c-112">Usare questa proprietà per configurare l'origine del supporto WTV.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-112">Use this property to configure the WTV media source.</span></span> <span data-ttu-id="6fa5c-113">Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="6fa5c-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="6fa5c-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="6fa5c-115">L'origine multimediale WTV legge i file di Windows registrato TV (con estensione wtv e MS-DRV).</span><span class="sxs-lookup"><span data-stu-id="6fa5c-115">The WTV media source reads Windows Recorded TV Show (.wtv and .ms-drv) files.</span></span>

<span data-ttu-id="6fa5c-116">Questa proprietà deve avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-116">This property must have one of the following values.</span></span>

-   <span data-ttu-id="6fa5c-117">1: esegue il mapping dei flussi audio disponibili a un singolo output, in base al sistema locale.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-117">1: Map available audio streams to a single output, based on the system local.</span></span> <span data-ttu-id="6fa5c-118">Questa modalità è appropriata per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-118">This mode is appropriate for playback.</span></span> <span data-ttu-id="6fa5c-119">(impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="6fa5c-119">(Default.)</span></span>
-   2. <span data-ttu-id="6fa5c-120">Vengono selezionati tutti i flussi audio e i sottoflussi, ad esempio didascalia e flussi di dati.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-120">All audio streams and substreams (such as caption and data streams) are selected.</span></span> <span data-ttu-id="6fa5c-121">Questa modalità è appropriata per la remuxing o la transcodifica.</span><span class="sxs-lookup"><span data-stu-id="6fa5c-121">This mode is appropriate for remuxing or transcoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa5c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fa5c-122">Requirements</span></span>



| <span data-ttu-id="6fa5c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fa5c-123">Requirement</span></span> | <span data-ttu-id="6fa5c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6fa5c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa5c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fa5c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa5c-126">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6fa5c-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6fa5c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fa5c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa5c-128">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="6fa5c-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6fa5c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fa5c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fa5c-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa5c-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa5c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fa5c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa5c-132">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6fa5c-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
