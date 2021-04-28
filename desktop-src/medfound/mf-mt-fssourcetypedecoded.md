---
description: "MF_MT_FSSourceTypeDecoded attributo : specifica se un decodificatore può usare timestamp di decodifica (DTS) durante l'impostazione dei timestamp."
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093089"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="e9595-103">Attributo MF \_ MT \_ FSSourceTypeDecoded</span><span class="sxs-lookup"><span data-stu-id="e9595-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="e9595-104">Specifica che un tipo di supporto viene decodificato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e9595-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="e9595-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e9595-105">Data type</span></span>

<span data-ttu-id="e9595-106">**BOOL** archiviato come **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e9595-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="e9595-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9595-107">Remarks</span></span>
<span data-ttu-id="e9595-108">Un tipo di supporto è contrassegnato come attributo per indicare che non esiste nell'origine fisica ed è sintetizzato dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="e9595-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="e9595-109">Il valore 1 (TRUE) indica che il tipo di supporto è sintetizzato.</span><span class="sxs-lookup"><span data-stu-id="e9595-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="e9595-110">Il valore 0 (FALSE) o il valore non presente indica che non lo è.</span><span class="sxs-lookup"><span data-stu-id="e9595-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="e9595-111">Nella versione corrente questo attributo deve essere specificato usando il valore GUID seguente anziché la costante MD_MT_FSSourceTypeDecoded seguente:</span><span class="sxs-lookup"><span data-stu-id="e9595-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="e9595-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9595-112">Requirements</span></span>



| <span data-ttu-id="e9595-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9595-113">Requirement</span></span> | <span data-ttu-id="e9595-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e9595-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9595-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9595-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e9595-116">Windows 8 app \[ desktop \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e9595-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e9595-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9595-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e9595-118">App desktop di Windows Server 2012 \[ \| per app UWP\]</span><span class="sxs-lookup"><span data-stu-id="e9595-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="e9595-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9595-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9595-120">Elenco alfabetico degli Media Foundation personalizzati</span><span class="sxs-lookup"><span data-stu-id="e9595-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




