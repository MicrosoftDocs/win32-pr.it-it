---
description: Specifica i criteri di controllo di un plug-in locale.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: Attributo MF_LOCAL_PLUGIN_CONTROL_POLICY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319608"
---
# <a name="mf_local_plugin_control_policy-attribute"></a><span data-ttu-id="2abc7-103">\_Attributo dei \_ criteri di controllo del plug-in locale MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="2abc7-103">MF\_LOCAL\_PLUGIN\_CONTROL\_POLICY attribute</span></span>

<span data-ttu-id="2abc7-104">Specifica i criteri di controllo di un plug-in locale.</span><span class="sxs-lookup"><span data-stu-id="2abc7-104">Specifies a local plugin control policy.</span></span>

## <a name="data-type"></a><span data-ttu-id="2abc7-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2abc7-105">Data type</span></span>

<span data-ttu-id="2abc7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2abc7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2abc7-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2abc7-107">Remarks</span></span>

<span data-ttu-id="2abc7-108">Impostare questo attributo su uno dei valori [**dei \_ \_ \_ criteri di controllo del plug**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) -in MF.</span><span class="sxs-lookup"><span data-stu-id="2abc7-108">Set this attribute to one of the [**MF\_PLUGIN\_CONTROL\_POLICY**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) values.</span></span>

<span data-ttu-id="2abc7-109">Questo attributo consente all'app di specificare un criterio locale più restrittivo rispetto ai criteri a livello di processo configurati da [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span><span class="sxs-lookup"><span data-stu-id="2abc7-109">This attributes allows the app to specify a more restrictive local policy than the process-wide policy configured by [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span></span>

## <a name="requirements"></a><span data-ttu-id="2abc7-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2abc7-110">Requirements</span></span>



| <span data-ttu-id="2abc7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abc7-111">Requirement</span></span> | <span data-ttu-id="2abc7-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2abc7-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2abc7-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2abc7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2abc7-114">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2abc7-114">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2abc7-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2abc7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2abc7-116">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2abc7-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2abc7-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2abc7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2abc7-118"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2abc7-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2abc7-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2abc7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2abc7-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2abc7-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2abc7-121">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="2abc7-121">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




