---
description: Il metodo SourceListAddSource aggiunge un'origine di rete o URL. Accetta SourcePath, Type e index come parametri. Questo metodo chiama MsiSourceListAddSourceEx.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Patch. SourceListAddSource, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc0a3bc0d966ec6836d1523745b296350562aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327317"
---
# <a name="patchsourcelistaddsource-method"></a><span data-ttu-id="71160-105">Patch. SourceListAddSource, metodo</span><span class="sxs-lookup"><span data-stu-id="71160-105">Patch.SourceListAddSource method</span></span>

<span data-ttu-id="71160-106">Il metodo **SourceListAddSource** aggiunge un'origine di rete o URL.</span><span class="sxs-lookup"><span data-stu-id="71160-106">The **SourceListAddSource** method adds a network or URL source.</span></span> <span data-ttu-id="71160-107">Accetta *SourcePath*, *Type* e *index* come parametri.</span><span class="sxs-lookup"><span data-stu-id="71160-107">Accepts *SourcePath*, *Type* and *Index* as parameters.</span></span> <span data-ttu-id="71160-108">Questo metodo chiama [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span><span class="sxs-lookup"><span data-stu-id="71160-108">This method calls [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="71160-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71160-109">Syntax</span></span>


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a><span data-ttu-id="71160-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="71160-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71160-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="71160-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="71160-112">Tipo di origine da aggiungere: MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="71160-112">Type of source to be added: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="71160-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="71160-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="71160-114">Percorso dell'origine da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="71160-114">Path to the source to be added.</span></span>

</dd> <dt>

<span data-ttu-id="71160-115">*Index*</span><span class="sxs-lookup"><span data-stu-id="71160-115">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="71160-116">Se **SourceListAddSource** viene chiamato con una nuova origine e un *Indice* impostati su 0, il programma di installazione aggiunge l'origine alla fine dell'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="71160-116">If **SourceListAddSource** is called with a new source and *Index* set to 0, the installer adds the source to the end of the source list.</span></span>

<span data-ttu-id="71160-117">Se questa funzione viene chiamata con un'origine già esistente nell'elenco di origine e *index* è impostato su 0, il programma di installazione mantiene l'indice esistente dell'origine.</span><span class="sxs-lookup"><span data-stu-id="71160-117">If this function is called with a source already existing in the source list and *Index* is set to 0, the installer retains the source's existing index.</span></span>

<span data-ttu-id="71160-118">Se la funzione viene chiamata con un'origine esistente nell'elenco di origine e *index* è impostato su un valore diverso da zero, l'origine viene rimossa dalla posizione corrente nell'elenco e inserita in corrispondenza della posizione specificata da *index*, prima di qualsiasi origine già esistente in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="71160-118">If the function is called with an existing source in the source list and *Index* is set to a non-zero value, the source is removed from its current location in the list and inserted at the position specified by *Index*, before any source that already exists at that position.</span></span>

<span data-ttu-id="71160-119">Se la funzione viene chiamata con una nuova origine e *index* è impostato su un valore diverso da zero, l'origine viene inserita in corrispondenza della posizione specificata da *index*, prima di qualsiasi origine già presente in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="71160-119">If the function is called with a new source and *Index* is set to a non-zero value, the source is inserted at the position specified by *Index*, before any source that already exists at that position.</span></span> <span data-ttu-id="71160-120">Il valore di indice per tutte le origini nell'elenco dopo l'indice specificato dall' *Indice* viene aggiornato per garantire che i valori di indice univoci e l'ordine preesistente rimangano invariati.</span><span class="sxs-lookup"><span data-stu-id="71160-120">The index value for all sources in the list after the index specified by *Index* are updated to ensure unique index values and the preexisting order is guaranteed to remain unchanged.</span></span>

<span data-ttu-id="71160-121">Se l' *Indice* è maggiore del numero di origini nell'elenco, l'origine viene posizionata alla fine dell'elenco con un valore di indice maggiore di quello di un'origine esistente.</span><span class="sxs-lookup"><span data-stu-id="71160-121">If *Index* is greater than the number of sources in the list, the source is placed at the end of the list with an index value one larger than any existing source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71160-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71160-122">Return value</span></span>

<span data-ttu-id="71160-123">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="71160-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="71160-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71160-124">Requirements</span></span>



| <span data-ttu-id="71160-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="71160-125">Requirement</span></span> | <span data-ttu-id="71160-126">Valore</span><span class="sxs-lookup"><span data-stu-id="71160-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71160-127">Versione</span><span class="sxs-lookup"><span data-stu-id="71160-127">Version</span></span><br/> | <span data-ttu-id="71160-128">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71160-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="71160-129">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="71160-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="71160-130">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="71160-130">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="71160-131">DLL</span><span class="sxs-lookup"><span data-stu-id="71160-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="71160-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71160-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="71160-133">IID</span><span class="sxs-lookup"><span data-stu-id="71160-133">IID</span></span><br/>     | <span data-ttu-id="71160-134">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="71160-134">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="71160-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71160-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71160-136">**Patch**</span><span class="sxs-lookup"><span data-stu-id="71160-136">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="71160-137">**MsiSourceListAddSourceEx**</span><span class="sxs-lookup"><span data-stu-id="71160-137">**MsiSourceListAddSourceEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[<span data-ttu-id="71160-138">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="71160-138">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




