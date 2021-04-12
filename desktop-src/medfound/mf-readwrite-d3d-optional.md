---
description: Specifica se l'applicazione richiede il supporto di Microsoft Direct3D nel lettore di origine o del sink.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: Attributo MF_READWRITE_D3D_OPTIONAL (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233743"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a><span data-ttu-id="607b2-103">\_Attributo facoltativo di MF ReadWrite \_ D3D \_</span><span class="sxs-lookup"><span data-stu-id="607b2-103">MF\_READWRITE\_D3D\_OPTIONAL attribute</span></span>

<span data-ttu-id="607b2-104">Specifica se l'applicazione richiede il supporto di Microsoft Direct3D nel [lettore di origine](source-reader.md) o del [sink](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="607b2-104">Specifies whether the application requires Microsoft Direct3D support in the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="607b2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="607b2-105">Data type</span></span>

<span data-ttu-id="607b2-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="607b2-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="607b2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="607b2-107">Remarks</span></span>

<span data-ttu-id="607b2-108">Questo attributo si applica solo se l'applicazione Abilita il supporto Direct3D usando l'attributo gestione [ \_ D3D del lettore di origine \_ \_ \_ MF](mf-source-reader-d3d-manager.md) o il [ \_ \_ \_ \_ gestore D3D sink writer](mf-sink-writer-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="607b2-108">This attribute applies only if the application enables Direct3D support using the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) or [MF\_SINK\_WRITER\_D3D\_MANAGER](mf-sink-writer-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="607b2-109">Se l'applicazione Abilita il supporto Direct3D, il writer di origine e di sink tenterà di allocare le superfici Direct3D per i video.</span><span class="sxs-lookup"><span data-stu-id="607b2-109">If the application enables Direct3D support, the Source Reader and Sink Writer will both try to allocate Direct3D surfaces for video.</span></span> <span data-ttu-id="607b2-110">Se l'operazione ha esito negativo e l' \_ \_ \_ attributo facoltativo ReadWrite D3D è **true**, il writer di lettura/sink di origine eseguirà il fallback per l'allocazione di superfici video nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="607b2-110">If this fails, and the MF\_READWRITE\_D3D\_OPTIONAL attribute is **TRUE**, the Source Reader/Sink Writer will fall back to allocating video surfaces in system memory.</span></span> <span data-ttu-id="607b2-111">In caso contrario, se non è possibile allocare le superfici Direct3D e \_ \_ l'opzione MF ReadWrite D3D \_ optional è **false**, si verifica un errore durante l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="607b2-111">Otherwise, if Direct3D surfaces cannot be allocated and MF\_READWRITE\_D3D\_OPTIONAL is **FALSE**, an error occurs during processing.</span></span>

<span data-ttu-id="607b2-112">Se l'applicazione non Abilita il supporto Direct3D, il writer di lettura/sink di origine utilizza la memoria di sistema e ignora il valore di MF \_ ReadWrite \_ D3D \_ Optional.</span><span class="sxs-lookup"><span data-stu-id="607b2-112">If the application does not enable Direct3D support, the Source Reader/Sink Writer uses system memory, and ignores the value of MF\_READWRITE\_D3D\_OPTIONAL.</span></span>

<span data-ttu-id="607b2-113">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="607b2-113">This attribute is optional.</span></span> <span data-ttu-id="607b2-114">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="607b2-114">The default value is **FALSE**.</span></span> <span data-ttu-id="607b2-115">Impostare l'attributo quando si crea il Reader di origine o il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="607b2-115">Set the attribute when you create the Source Reader or Sink Writer.</span></span>

## <a name="requirements"></a><span data-ttu-id="607b2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="607b2-116">Requirements</span></span>



| <span data-ttu-id="607b2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="607b2-117">Requirement</span></span> | <span data-ttu-id="607b2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="607b2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="607b2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="607b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="607b2-120">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="607b2-120">Windows 8 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="607b2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="607b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="607b2-122">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="607b2-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="607b2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="607b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="607b2-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="607b2-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607b2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="607b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607b2-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="607b2-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="607b2-127">Attributi del writer di sink</span><span class="sxs-lookup"><span data-stu-id="607b2-127">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="607b2-128">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="607b2-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




