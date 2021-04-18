---
description: Specifica se un decodificatore può utilizzare i timestamp di decodifica (DTS) quando si configurano i timestamp.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319607"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="a358b-103">\_Attributo MF mt \_ FSSourceTypeDecoded</span><span class="sxs-lookup"><span data-stu-id="a358b-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="a358b-104">Specifica che un tipo di supporto è decodificato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a358b-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="a358b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a358b-105">Data type</span></span>

<span data-ttu-id="a358b-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a358b-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="a358b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a358b-107">Remarks</span></span>
<span data-ttu-id="a358b-108">Un tipo di supporto è contrassegnato come un attributo per indicare che non esiste nell'origine fisica ed è sintetizzato dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="a358b-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="a358b-109">Il valore 1 (TRUE) indica che il tipo di supporto è sintetizzato.</span><span class="sxs-lookup"><span data-stu-id="a358b-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="a358b-110">Il valore 0 (FALSE) o il valore non presente indica che non lo è.</span><span class="sxs-lookup"><span data-stu-id="a358b-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="a358b-111">Nella versione corrente, questo attributo deve essere specificato usando il valore GUID seguente anziché la costante MD_MT_FSSourceTypeDecoded:</span><span class="sxs-lookup"><span data-stu-id="a358b-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="a358b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a358b-112">Requirements</span></span>



| <span data-ttu-id="a358b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a358b-113">Requirement</span></span> | <span data-ttu-id="a358b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a358b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a358b-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a358b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a358b-116">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a358b-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a358b-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a358b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a358b-118">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="a358b-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="a358b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a358b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a358b-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a358b-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




