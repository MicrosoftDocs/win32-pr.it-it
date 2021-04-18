---
description: La proprietà SourceListInfo dell'oggetto patch ottiene e imposta le proprietà delle informazioni di origine per una patch. Questa proprietà chiama MsiSourceListGetInfo o MsiSourceListSetInfo. Si tratta di una proprietà di lettura o scrittura.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Proprietà patch. SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325894"
---
# <a name="patchsourcelistinfo-property"></a><span data-ttu-id="9d2ed-105">Proprietà patch. SourceListInfo</span><span class="sxs-lookup"><span data-stu-id="9d2ed-105">Patch.SourceListInfo property</span></span>

<span data-ttu-id="9d2ed-106">La proprietà **SourceListInfo** dell'oggetto [**patch**](patch-object.md) ottiene e imposta le proprietà delle informazioni di origine per una patch.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-106">The **SourceListInfo** property of the [**Patch**](patch-object.md) object gets and sets the source information properties for a patch.</span></span> <span data-ttu-id="9d2ed-107">Questa proprietà chiama [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) o [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="9d2ed-107">This property call [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="9d2ed-108">Si tratta di una proprietà di lettura o scrittura.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-108">This is a read or write property.</span></span>

<span data-ttu-id="9d2ed-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d2ed-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d2ed-110">Syntax</span></span>


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="9d2ed-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9d2ed-111">Property value</span></span>

<span data-ttu-id="9d2ed-112">Nome delle proprietà delle informazioni di origine per una patch su cui eseguire una query o un set.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-112">The name of the source information properties for a patch to query or set.</span></span> <span data-ttu-id="9d2ed-113">Per i valori possibili, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d2ed-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d2ed-114">Remarks</span></span>

<span data-ttu-id="9d2ed-115">Non è possibile impostare tutte le proprietà che possono essere recuperate.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="9d2ed-116">Il parametro *szProperty* può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="9d2ed-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d2ed-117">Property</span></span>         | <span data-ttu-id="9d2ed-118">È possibile impostare?</span><span class="sxs-lookup"><span data-stu-id="9d2ed-118">Can set?</span></span> | <span data-ttu-id="9d2ed-119">Significato</span><span class="sxs-lookup"><span data-stu-id="9d2ed-119">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d2ed-120">MediaPackagePath</span><span class="sxs-lookup"><span data-stu-id="9d2ed-120">MediaPackagePath</span></span> | <span data-ttu-id="9d2ed-121">S</span><span class="sxs-lookup"><span data-stu-id="9d2ed-121">Y</span></span>        | <span data-ttu-id="9d2ed-122">Percorso relativo alla radice del supporto di installazione.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="9d2ed-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="9d2ed-123">DiskPrompt</span></span>       | <span data-ttu-id="9d2ed-124">S</span><span class="sxs-lookup"><span data-stu-id="9d2ed-124">Y</span></span>        | <span data-ttu-id="9d2ed-125">Modello di richiesta utilizzato quando viene richiesto all'utente il supporto di installazione.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="9d2ed-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="9d2ed-126">LastUsedSource</span></span>   | <span data-ttu-id="9d2ed-127">S</span><span class="sxs-lookup"><span data-stu-id="9d2ed-127">Y</span></span>        | <span data-ttu-id="9d2ed-128">Il percorso di origine usato più di recente per la patch.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-128">The most recently used source location for the patch.</span></span> <span data-ttu-id="9d2ed-129">Quando si imposta questa proprietà, anteporre il prefisso "n;" al percorso di origine di rete o "u;" per il tipo di URL.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="9d2ed-130">Ad esempio, usare "n; \\ \\ Scratch \\ Scratch \\ test "o" u; https://microsoft.com/Patches/Office/SP1 ".</span><span class="sxs-lookup"><span data-stu-id="9d2ed-130">For example, use "n;\\\\scratch\\scratch\\test" or "u;https://microsoft.com/Patches/Office/SP1".</span></span> |
| <span data-ttu-id="9d2ed-131">LastUsedType</span><span class="sxs-lookup"><span data-stu-id="9d2ed-131">LastUsedType</span></span>     | <span data-ttu-id="9d2ed-132">N</span><span class="sxs-lookup"><span data-stu-id="9d2ed-132">N</span></span>        | <span data-ttu-id="9d2ed-133">"n" se l'ultima origine usata è un percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="9d2ed-134">"u" se l'ultima origine usata era un percorso URL.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="9d2ed-135">"m" se l'ultima origine usata era un supporto.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-135">"m" if the last used source was media.</span></span> <span data-ttu-id="9d2ed-136">Stringa vuota ("") se non è disponibile l'ultima origine usata.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-136">Empty string ("") if there is no last used source.</span></span>                                                                      |
| <span data-ttu-id="9d2ed-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="9d2ed-137">PackageName</span></span>      | <span data-ttu-id="9d2ed-138">S</span><span class="sxs-lookup"><span data-stu-id="9d2ed-138">Y</span></span>        | <span data-ttu-id="9d2ed-139">Nome del pacchetto di Windows Installer o del pacchetto di patch nell'origine.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="9d2ed-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d2ed-140">Requirements</span></span>



| <span data-ttu-id="9d2ed-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d2ed-141">Requirement</span></span> | <span data-ttu-id="9d2ed-142">Valore</span><span class="sxs-lookup"><span data-stu-id="9d2ed-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d2ed-143">Versione</span><span class="sxs-lookup"><span data-stu-id="9d2ed-143">Version</span></span><br/> | <span data-ttu-id="9d2ed-144">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9d2ed-145">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9d2ed-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9d2ed-146">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9d2ed-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="9d2ed-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9d2ed-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="9d2ed-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d2ed-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="9d2ed-149">IID</span><span class="sxs-lookup"><span data-stu-id="9d2ed-149">IID</span></span><br/>     | <span data-ttu-id="9d2ed-150">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9d2ed-150">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="9d2ed-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d2ed-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d2ed-152">**Patch**</span><span class="sxs-lookup"><span data-stu-id="9d2ed-152">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="9d2ed-153">**MsiSourceListGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9d2ed-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="9d2ed-154">**MsiSourceListSetInfo**</span><span class="sxs-lookup"><span data-stu-id="9d2ed-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="9d2ed-155">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="9d2ed-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




