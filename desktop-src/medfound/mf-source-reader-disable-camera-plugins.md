---
description: Disabilita l'uso dei plug-in della fotocamera di post-elaborazione da parte del lettore di origine.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: Attributo MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233620"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a><span data-ttu-id="ab084-103">\_Attributo MF Source \_ Reader \_ Disable \_ fotocamera \_ plugins</span><span class="sxs-lookup"><span data-stu-id="ab084-103">MF\_SOURCE\_READER\_DISABLE\_CAMERA\_PLUGINS attribute</span></span>

<span data-ttu-id="ab084-104">Disabilita l'uso dei plug-in della fotocamera di post-elaborazione da parte del [lettore di origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="ab084-104">Disables the use of post-processing camera plug-ins by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="ab084-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ab084-105">Data type</span></span>

<span data-ttu-id="ab084-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab084-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ab084-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab084-107">Remarks</span></span>

<span data-ttu-id="ab084-108">Questo attributo si applica quando il lettore di origine viene usato con un'origine di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="ab084-108">This attribute applies when the Source Reader is used with a video capture source.</span></span> <span data-ttu-id="ab084-109">Se questo attributo è **true**, impedisce al lettore di origine di caricare tutti i plug-in di post-elaborazione che potrebbero essere forniti dalla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="ab084-109">If this attribute is **TRUE**, it prevents the Source Reader from loading any post-processing plug-ins that the camera might provide.</span></span> <span data-ttu-id="ab084-110">In caso contrario, per impostazione predefinita il lettore di origine li caricherà.</span><span class="sxs-lookup"><span data-stu-id="ab084-110">Otherwise, by default the Source Reader will load them.</span></span>

<span data-ttu-id="ab084-111">Il valore predefinito di questo attributo è **false**.</span><span class="sxs-lookup"><span data-stu-id="ab084-111">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="ab084-112">Impostare l'attributo quando si crea il lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="ab084-112">Set the attribute when you create the source reader.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab084-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab084-113">Requirements</span></span>



| <span data-ttu-id="ab084-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab084-114">Requirement</span></span> | <span data-ttu-id="ab084-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ab084-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab084-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab084-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab084-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ab084-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ab084-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab084-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab084-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="ab084-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ab084-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab084-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab084-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab084-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab084-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab084-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab084-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab084-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ab084-124">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="ab084-124">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




