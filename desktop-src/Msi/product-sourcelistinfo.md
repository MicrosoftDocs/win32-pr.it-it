---
description: La proprietà SourceListInfo dell'oggetto Product ottiene e imposta le proprietà delle informazioni di origine per un prodotto. Questa proprietà chiama MsiSourceListGetInfo o MsiSourceListSetInfo. Si tratta di una proprietà di lettura o scrittura.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Proprietà Product. SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330624"
---
# <a name="productsourcelistinfo-property"></a><span data-ttu-id="63d6f-105">Proprietà Product. SourceListInfo</span><span class="sxs-lookup"><span data-stu-id="63d6f-105">Product.SourceListInfo property</span></span>

<span data-ttu-id="63d6f-106">La proprietà **SourceListInfo** dell'oggetto [**Product**](product-object.md) ottiene e imposta le proprietà delle informazioni di origine per un prodotto.</span><span class="sxs-lookup"><span data-stu-id="63d6f-106">The **SourceListInfo** property of the [**Product**](product-object.md) object gets and sets the source information properties for a product.</span></span> <span data-ttu-id="63d6f-107">Questa proprietà chiama [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) o [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="63d6f-107">This property calls [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="63d6f-108">Si tratta di una proprietà di lettura o scrittura.</span><span class="sxs-lookup"><span data-stu-id="63d6f-108">This is a read or write property.</span></span>

<span data-ttu-id="63d6f-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="63d6f-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d6f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63d6f-110">Syntax</span></span>


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="63d6f-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="63d6f-111">Property value</span></span>

<span data-ttu-id="63d6f-112">Nome delle proprietà delle informazioni di origine per un prodotto da interrogare o impostare.</span><span class="sxs-lookup"><span data-stu-id="63d6f-112">The name of the source information properties for a product to query or set.</span></span> <span data-ttu-id="63d6f-113">Per i valori possibili, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="63d6f-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="63d6f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="63d6f-114">Remarks</span></span>

<span data-ttu-id="63d6f-115">Non è possibile impostare tutte le proprietà che possono essere recuperate.</span><span class="sxs-lookup"><span data-stu-id="63d6f-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="63d6f-116">Il parametro *szProperty* può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="63d6f-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="63d6f-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="63d6f-117">Property</span></span>         | <span data-ttu-id="63d6f-118">È possibile impostare?</span><span class="sxs-lookup"><span data-stu-id="63d6f-118">Can set?</span></span> | <span data-ttu-id="63d6f-119">Significato</span><span class="sxs-lookup"><span data-stu-id="63d6f-119">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d6f-120">MediaPackagePath</span><span class="sxs-lookup"><span data-stu-id="63d6f-120">MediaPackagePath</span></span> | <span data-ttu-id="63d6f-121">S</span><span class="sxs-lookup"><span data-stu-id="63d6f-121">Y</span></span>        | <span data-ttu-id="63d6f-122">Percorso relativo alla radice del supporto di installazione.</span><span class="sxs-lookup"><span data-stu-id="63d6f-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="63d6f-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="63d6f-123">DiskPrompt</span></span>       | <span data-ttu-id="63d6f-124">S</span><span class="sxs-lookup"><span data-stu-id="63d6f-124">Y</span></span>        | <span data-ttu-id="63d6f-125">Modello di richiesta utilizzato quando viene richiesto all'utente il supporto di installazione.</span><span class="sxs-lookup"><span data-stu-id="63d6f-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="63d6f-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="63d6f-126">LastUsedSource</span></span>   | <span data-ttu-id="63d6f-127">S</span><span class="sxs-lookup"><span data-stu-id="63d6f-127">Y</span></span>        | <span data-ttu-id="63d6f-128">Il percorso di origine utilizzato più di recente per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="63d6f-128">The most recently used source location for the product.</span></span> <span data-ttu-id="63d6f-129">Quando si imposta questa proprietà, anteporre il prefisso "n;" al percorso di origine di rete o "u;" per il tipo di URL.</span><span class="sxs-lookup"><span data-stu-id="63d6f-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="63d6f-130">Ad esempio, "n; \\ \\ Scratch \\ My \\ source "e" u; https://MyServer/MyFolder/MySource ".</span><span class="sxs-lookup"><span data-stu-id="63d6f-130">For example, "n;\\\\scratch\\scratch\\MySource" and "u;https://MyServer/MyFolder/MySource".</span></span> |
| <span data-ttu-id="63d6f-131">LastUsedType</span><span class="sxs-lookup"><span data-stu-id="63d6f-131">LastUsedType</span></span>     | <span data-ttu-id="63d6f-132">N</span><span class="sxs-lookup"><span data-stu-id="63d6f-132">N</span></span>        | <span data-ttu-id="63d6f-133">"n" se l'ultima origine usata è un percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="63d6f-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="63d6f-134">"u" se l'ultima origine usata era un percorso URL.</span><span class="sxs-lookup"><span data-stu-id="63d6f-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="63d6f-135">"m" se l'ultima origine usata era un supporto.</span><span class="sxs-lookup"><span data-stu-id="63d6f-135">"m" if the last used source was media.</span></span> <span data-ttu-id="63d6f-136">Stringa vuota ("") se non è disponibile l'ultima origine usata.</span><span class="sxs-lookup"><span data-stu-id="63d6f-136">Empty string ("") if there is no last used source.</span></span>                                                                   |
| <span data-ttu-id="63d6f-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="63d6f-137">PackageName</span></span>      | <span data-ttu-id="63d6f-138">S</span><span class="sxs-lookup"><span data-stu-id="63d6f-138">Y</span></span>        | <span data-ttu-id="63d6f-139">Nome del pacchetto di Windows Installer o del pacchetto di patch nell'origine.</span><span class="sxs-lookup"><span data-stu-id="63d6f-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="63d6f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63d6f-140">Requirements</span></span>



| <span data-ttu-id="63d6f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="63d6f-141">Requirement</span></span> | <span data-ttu-id="63d6f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="63d6f-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d6f-143">Versione</span><span class="sxs-lookup"><span data-stu-id="63d6f-143">Version</span></span><br/> | <span data-ttu-id="63d6f-144">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="63d6f-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="63d6f-145">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="63d6f-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="63d6f-146">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="63d6f-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="63d6f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="63d6f-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="63d6f-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63d6f-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="63d6f-149">IID</span><span class="sxs-lookup"><span data-stu-id="63d6f-149">IID</span></span><br/>     | <span data-ttu-id="63d6f-150">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="63d6f-150">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="63d6f-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63d6f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d6f-152">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="63d6f-152">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="63d6f-153">**MsiSourceListGetInfo**</span><span class="sxs-lookup"><span data-stu-id="63d6f-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="63d6f-154">**MsiSourceListSetInfo**</span><span class="sxs-lookup"><span data-stu-id="63d6f-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="63d6f-155">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="63d6f-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




