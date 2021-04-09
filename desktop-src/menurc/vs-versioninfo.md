---
title: Struttura VS_VERSIONINFO
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Si tratta della struttura radice che contiene tutte le altre strutture di informazioni sulla versione del file.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- Menu struttura VS_VERSIONINFO e altre risorse
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121426"
---
# <a name="vs_versioninfo-structure"></a><span data-ttu-id="088ef-105">Struttura di VS \_ VERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="088ef-105">VS\_VERSIONINFO structure</span></span>

<span data-ttu-id="088ef-106">Rappresenta l'organizzazione dei dati in una risorsa di versione del file.</span><span class="sxs-lookup"><span data-stu-id="088ef-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="088ef-107">Si tratta della struttura radice che contiene tutte le altre strutture di informazioni sulla versione del file.</span><span class="sxs-lookup"><span data-stu-id="088ef-107">It is the root structure that contains all other file-version information structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="088ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="088ef-108">Syntax</span></span>


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="088ef-109">Members</span><span class="sxs-lookup"><span data-stu-id="088ef-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="088ef-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="088ef-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="088ef-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="088ef-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="088ef-112">Lunghezza, in byte, della struttura di **Visual Studio \_ VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="088ef-112">The length, in bytes, of the **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="088ef-113">Questa lunghezza non include alcun riempimento che allinea i dati delle risorse della versione successiva in un limite di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="088ef-113">This length does not include any padding that aligns any subsequent version resource data on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="088ef-114">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="088ef-114">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="088ef-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="088ef-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="088ef-116">Lunghezza, in byte, del membro del **valore** .</span><span class="sxs-lookup"><span data-stu-id="088ef-116">The length, in bytes, of the **Value** member.</span></span> <span data-ttu-id="088ef-117">Questo valore è zero se non è presente alcun membro di **valore** associato alla struttura della versione corrente.</span><span class="sxs-lookup"><span data-stu-id="088ef-117">This value is zero if there is no **Value** member associated with the current version structure.</span></span>

</dd> <dt>

<span data-ttu-id="088ef-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="088ef-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="088ef-119">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="088ef-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="088ef-120">Tipo di dati nella risorsa della versione.</span><span class="sxs-lookup"><span data-stu-id="088ef-120">The type of data in the version resource.</span></span> <span data-ttu-id="088ef-121">Questo membro è 1 se la risorsa della versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.</span><span class="sxs-lookup"><span data-stu-id="088ef-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="088ef-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="088ef-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="088ef-123">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="088ef-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="088ef-124">Stringa Unicode L "informazioni sulla \_ versione di vs \_ ".</span><span class="sxs-lookup"><span data-stu-id="088ef-124">The Unicode string L"VS\_VERSION\_INFO".</span></span>

</dd> <dt>

<span data-ttu-id="088ef-125">**Padding1**</span><span class="sxs-lookup"><span data-stu-id="088ef-125">**Padding1**</span></span>
</dt> <dd>

<span data-ttu-id="088ef-126">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="088ef-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="088ef-127">Contiene un numero di parole pari a zero, se necessario, per allineare il membro del **valore** a un limite di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="088ef-127">Contains as many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="088ef-128">**Valore**</span><span class="sxs-lookup"><span data-stu-id="088ef-128">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="088ef-129">Tipo: **[ **vs \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span><span class="sxs-lookup"><span data-stu-id="088ef-129">Type: **[**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span></span>

</dd> <dd>

<span data-ttu-id="088ef-130">Dati arbitrari associati a questa struttura di **Visual Studio \_ VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="088ef-130">Arbitrary data associated with this **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="088ef-131">Il membro **wValueLength** specifica la lunghezza di questo membro. Se **wValueLength** è zero, questo membro non esiste.</span><span class="sxs-lookup"><span data-stu-id="088ef-131">The **wValueLength** member specifies the length of this member; if **wValueLength** is zero, this member does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="088ef-132">**Padding2**</span><span class="sxs-lookup"><span data-stu-id="088ef-132">**Padding2**</span></span>
</dt> <dd>

<span data-ttu-id="088ef-133">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="088ef-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="088ef-134">Il numero di parole necessarie per allineare il membro **figlio** al limite di 32 bit è pari a zero.</span><span class="sxs-lookup"><span data-stu-id="088ef-134">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span> <span data-ttu-id="088ef-135">Questi byte non sono inclusi in **wValueLength**.</span><span class="sxs-lookup"><span data-stu-id="088ef-135">These bytes are not included in **wValueLength**.</span></span> <span data-ttu-id="088ef-136">Questo membro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="088ef-136">This member is optional.</span></span>

</dd> <dt>

<span data-ttu-id="088ef-137">**Children**</span><span class="sxs-lookup"><span data-stu-id="088ef-137">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="088ef-138">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="088ef-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="088ef-139">Matrice di zero o una struttura [**StringFileInfo**](stringfileinfo.md) e zero o una struttura [**VarFileInfo**](varfileinfo.md) che sono elementi figlio della struttura corrente di **vs \_ VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="088ef-139">An array of zero or one [**StringFileInfo**](stringfileinfo.md) structures, and zero or one [**VarFileInfo**](varfileinfo.md) structures that are children of the current **VS\_VERSIONINFO** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="088ef-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="088ef-140">Remarks</span></span>

<span data-ttu-id="088ef-141">Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="088ef-141">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="088ef-142">Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="088ef-142">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="088ef-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="088ef-143">Requirements</span></span>



| <span data-ttu-id="088ef-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="088ef-144">Requirement</span></span> | <span data-ttu-id="088ef-145">Valore</span><span class="sxs-lookup"><span data-stu-id="088ef-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="088ef-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="088ef-146">Minimum supported client</span></span><br/> | <span data-ttu-id="088ef-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="088ef-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="088ef-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="088ef-148">Minimum supported server</span></span><br/> | <span data-ttu-id="088ef-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="088ef-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="088ef-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="088ef-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="088ef-151">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="088ef-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="088ef-152">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="088ef-152">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="088ef-153">**VerQueryValue**</span><span class="sxs-lookup"><span data-stu-id="088ef-153">**VerQueryValue**</span></span>](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[<span data-ttu-id="088ef-154">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="088ef-154">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="088ef-155">**VS \_ informazione FixedFileInfo**</span><span class="sxs-lookup"><span data-stu-id="088ef-155">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

<span data-ttu-id="088ef-156">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="088ef-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="088ef-157">Informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="088ef-157">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





