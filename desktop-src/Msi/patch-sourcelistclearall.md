---
description: Il metodo SourceListClearAll dell'oggetto patch cancella l'elenco di origine completo di tutte le origini del tipo specificato per una patch. Accetta il tipo come parametro. Questo metodo chiama MsiSourceListClearAllEx.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Patch. SourceListClearAll, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329615"
---
# <a name="patchsourcelistclearall-method"></a><span data-ttu-id="1a7d2-105">Patch. SourceListClearAll, metodo</span><span class="sxs-lookup"><span data-stu-id="1a7d2-105">Patch.SourceListClearAll method</span></span>

<span data-ttu-id="1a7d2-106">Il metodo **SourceListClearAll** dell'oggetto [**patch**](patch-object.md) cancella l'elenco di origine completo di tutte le origini del tipo specificato per una patch.</span><span class="sxs-lookup"><span data-stu-id="1a7d2-106">The **SourceListClearAll** method of the [**Patch**](patch-object.md) object clears the complete source list of all sources of the specified type for a patch.</span></span> <span data-ttu-id="1a7d2-107">Accetta il *tipo* come parametro.</span><span class="sxs-lookup"><span data-stu-id="1a7d2-107">Accepts *Type* as a parameter.</span></span> <span data-ttu-id="1a7d2-108">Questo metodo chiama [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span><span class="sxs-lookup"><span data-stu-id="1a7d2-108">This method calls [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a7d2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a7d2-109">Syntax</span></span>


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="1a7d2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a7d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a7d2-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="1a7d2-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="1a7d2-112">Tipo di origine, ad esempio rete, URL o supporto.</span><span class="sxs-lookup"><span data-stu-id="1a7d2-112">The type of source type, such as network, URL or media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a7d2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a7d2-113">Return value</span></span>

<span data-ttu-id="1a7d2-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1a7d2-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a7d2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a7d2-115">Requirements</span></span>



| <span data-ttu-id="1a7d2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a7d2-116">Requirement</span></span> | <span data-ttu-id="1a7d2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1a7d2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7d2-118">Versione</span><span class="sxs-lookup"><span data-stu-id="1a7d2-118">Version</span></span><br/> | <span data-ttu-id="1a7d2-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1a7d2-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1a7d2-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1a7d2-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1a7d2-121">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1a7d2-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="1a7d2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1a7d2-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a7d2-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a7d2-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="1a7d2-124">IID</span><span class="sxs-lookup"><span data-stu-id="1a7d2-124">IID</span></span><br/>     | <span data-ttu-id="1a7d2-125">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1a7d2-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="1a7d2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a7d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a7d2-127">**Patch**</span><span class="sxs-lookup"><span data-stu-id="1a7d2-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="1a7d2-128">**MsiSourceListClearAllEx**</span><span class="sxs-lookup"><span data-stu-id="1a7d2-128">**MsiSourceListClearAllEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[<span data-ttu-id="1a7d2-129">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="1a7d2-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




