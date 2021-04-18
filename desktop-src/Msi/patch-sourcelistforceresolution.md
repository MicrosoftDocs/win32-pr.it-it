---
description: Il metodo SourceListForceResolution Cancella la proprietà dell'ultima origine usata.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Patch. SourceListForceResolution, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325899"
---
# <a name="patchsourcelistforceresolution-method"></a><span data-ttu-id="5a774-103">Patch. SourceListForceResolution, metodo</span><span class="sxs-lookup"><span data-stu-id="5a774-103">Patch.SourceListForceResolution method</span></span>

<span data-ttu-id="5a774-104">Il metodo **SourceListForceResolution** Cancella la proprietà dell'ultima origine usata.</span><span class="sxs-lookup"><span data-stu-id="5a774-104">The **SourceListForceResolution** method clears the last used source property.</span></span> <span data-ttu-id="5a774-105">In questo modo il programma di installazione esegue la ricerca nell'elenco di origine di un'origine patch valida la volta successiva che è richiesta l'origine della patch.</span><span class="sxs-lookup"><span data-stu-id="5a774-105">This forces the installer to search the source list for a valid patch source the next time the patch source is required.</span></span> <span data-ttu-id="5a774-106">Ad esempio, il programma di installazione richiede l'origine della patch per eseguire un'installazione o una reinstallazione quando manca la copia della cache locale della patch.</span><span class="sxs-lookup"><span data-stu-id="5a774-106">For example, the installer requires the patch source to perform an installation or reinstallation when the local cache copy of the patch is missing.</span></span> <span data-ttu-id="5a774-107">Questo metodo chiama [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="5a774-107">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a774-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a774-108">Syntax</span></span>


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="5a774-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a774-109">Parameters</span></span>

<span data-ttu-id="5a774-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5a774-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a774-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a774-111">Return value</span></span>

<span data-ttu-id="5a774-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5a774-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a774-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a774-113">Requirements</span></span>



| <span data-ttu-id="5a774-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a774-114">Requirement</span></span> | <span data-ttu-id="5a774-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5a774-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a774-116">Versione</span><span class="sxs-lookup"><span data-stu-id="5a774-116">Version</span></span><br/> | <span data-ttu-id="5a774-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5a774-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5a774-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a774-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5a774-119">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5a774-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="5a774-120">DLL</span><span class="sxs-lookup"><span data-stu-id="5a774-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a774-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a774-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="5a774-122">IID</span><span class="sxs-lookup"><span data-stu-id="5a774-122">IID</span></span><br/>     | <span data-ttu-id="5a774-123">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5a774-123">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="5a774-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a774-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a774-125">**Patch**</span><span class="sxs-lookup"><span data-stu-id="5a774-125">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="5a774-126">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="5a774-126">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="5a774-127">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="5a774-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




