---
description: Il metodo SourceListForceResolution Cancella la proprietà LastUsedSource.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Metodo Product. SourceListForceResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330628"
---
# <a name="productsourcelistforceresolution-method"></a><span data-ttu-id="12f2f-103">Metodo Product. SourceListForceResolution</span><span class="sxs-lookup"><span data-stu-id="12f2f-103">Product.SourceListForceResolution method</span></span>

<span data-ttu-id="12f2f-104">Il metodo **SourceListForceResolution** Cancella la proprietà LastUsedSource.</span><span class="sxs-lookup"><span data-stu-id="12f2f-104">The **SourceListForceResolution** method clears the LastUsedSource property.</span></span> <span data-ttu-id="12f2f-105">In questo modo, il programma di installazione esegue la ricerca nell'elenco di origine di una fonte di prodotto valida la volta successiva che è richiesta un'origine, ad esempio quando il programma di installazione esegue un'installazione o una reinstallazione o quando il percorso è necessario per l'esecuzione di un componente dall'origine.</span><span class="sxs-lookup"><span data-stu-id="12f2f-105">This forces the installer to search the source list for a valid product source the next time a source is required, such as when the installer performs an installation or a reinstallation, or when the path is required for a component set to run from the source.</span></span>

<span data-ttu-id="12f2f-106">Questo metodo chiama [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="12f2f-106">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="12f2f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12f2f-107">Syntax</span></span>


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="12f2f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="12f2f-108">Parameters</span></span>

<span data-ttu-id="12f2f-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="12f2f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12f2f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12f2f-110">Return value</span></span>

<span data-ttu-id="12f2f-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="12f2f-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f2f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12f2f-112">Requirements</span></span>



| <span data-ttu-id="12f2f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="12f2f-113">Requirement</span></span> | <span data-ttu-id="12f2f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="12f2f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f2f-115">Versione</span><span class="sxs-lookup"><span data-stu-id="12f2f-115">Version</span></span><br/> | <span data-ttu-id="12f2f-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="12f2f-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="12f2f-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="12f2f-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="12f2f-118">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="12f2f-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="12f2f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="12f2f-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="12f2f-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12f2f-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="12f2f-121">IID</span><span class="sxs-lookup"><span data-stu-id="12f2f-121">IID</span></span><br/>     | <span data-ttu-id="12f2f-122">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="12f2f-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="12f2f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12f2f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f2f-124">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="12f2f-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="12f2f-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="12f2f-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="12f2f-126">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="12f2f-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




