---
title: Proprietà WSMan. Error (WSManDisp. h)
description: Ottiene informazioni aggiuntive sull'errore, in un flusso XML, per la chiamata precedente a un metodo WSMan se Gestione remota Windows servizio non è stato in grado di creare un oggetto sessione, un oggetto ConnectionOptions o un oggetto ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà errore
- Gestione remota Windows proprietà errore, oggetto WSMan
- Gestione remota Windows oggetto WSMan, proprietà Error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119854"
---
# <a name="wsmanerror-property"></a><span data-ttu-id="641c3-106">WSMan. Error (proprietà)</span><span class="sxs-lookup"><span data-stu-id="641c3-106">WSMan.Error property</span></span>

<span data-ttu-id="641c3-107">Ottiene informazioni aggiuntive sull'errore, in un flusso XML, per la chiamata precedente a un metodo [**WSMan**](wsman.md) se gestione remota Windows servizio non è stato in grado di creare un oggetto [**sessione**](session.md) , un oggetto [**ConnectionOptions**](connectionoptions.md) o un oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="641c3-107">Gets additional error information, in an XML stream, for the preceding call to a [**WSMan**](wsman.md) method if Windows Remote Management service was unable to create a [**Session**](session.md) object, a [**ConnectionOptions**](connectionoptions.md) object, or a [**ResourceLocator**](resourcelocator.md) object.</span></span>

<span data-ttu-id="641c3-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="641c3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="641c3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="641c3-109">Syntax</span></span>


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a><span data-ttu-id="641c3-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="641c3-110">Property value</span></span>

<span data-ttu-id="641c3-111">Rappresentazione XML delle informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="641c3-111">The XML representation of the error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="641c3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="641c3-112">Requirements</span></span>



| <span data-ttu-id="641c3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="641c3-113">Requirement</span></span> | <span data-ttu-id="641c3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="641c3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="641c3-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="641c3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="641c3-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="641c3-116">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="641c3-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="641c3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="641c3-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="641c3-118">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="641c3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="641c3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="641c3-120"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="641c3-120"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="641c3-121">IDL</span><span class="sxs-lookup"><span data-stu-id="641c3-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="641c3-122"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="641c3-122"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="641c3-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="641c3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="641c3-124"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="641c3-124"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="641c3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="641c3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="641c3-126"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="641c3-126"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="641c3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="641c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="641c3-128">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="641c3-128">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





