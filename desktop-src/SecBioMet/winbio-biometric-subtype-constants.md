---
title: Costanti WINBIO_BIOMETRIC_SUBTYPE (tipi WinBio \_ . h)
description: Fornire informazioni su una misura biometrica.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964442"
---
# <a name="winbio_biometric_subtype-constants"></a><span data-ttu-id="274f8-103">\_Costanti SOTTOtipi BIOmetrici WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="274f8-103">WINBIO\_BIOMETRIC\_SUBTYPE Constants</span></span>

<span data-ttu-id="274f8-104">**WINBIO \_ Le costanti dei \_ SOTTOtipi BIOmetrici** vengono usate in tutta la Windows Biometric Framework per fornire informazioni aggiuntive su una misurazione biometrica.</span><span class="sxs-lookup"><span data-stu-id="274f8-104">**WINBIO\_BIOMETRIC\_SUBTYPE** constants are used throughout the Windows Biometric Framework to provide additional information about a biometric measurement.</span></span> <span data-ttu-id="274f8-105">È possibile utilizzare le costanti seguenti quando non è richiesto alcun sottotipo o quando è necessario un sottotipo.</span><span class="sxs-lookup"><span data-stu-id="274f8-105">The following constants can be used when no subtype is required or when any subtype is required.</span></span>



| <span data-ttu-id="274f8-106">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="274f8-106">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="274f8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="274f8-107">Description</span></span>                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <span data-ttu-id="274f8-108"><dt>**WINBIO \_ Sottotipo \_ senza \_ informazioni**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="274f8-108"><dt>**WINBIO\_SUBTYPE\_NO\_INFORMATION**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="274f8-109">Nessuna informazione sul sottotipo.</span><span class="sxs-lookup"><span data-stu-id="274f8-109">No subtype information.</span></span><br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <span data-ttu-id="274f8-110"><dt>**WINBIO \_ Sottotipo \_ any**</dt> <dt>0xFF</dt></span><span class="sxs-lookup"><span data-stu-id="274f8-110"><dt>**WINBIO\_SUBTYPE\_ANY**</dt> <dt>0xFF</dt></span></span> </dl>                                   | <span data-ttu-id="274f8-111">Qualsiasi sottotipo.</span><span class="sxs-lookup"><span data-stu-id="274f8-111">Any subtype.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="274f8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="274f8-112">Remarks</span></span>

<span data-ttu-id="274f8-113">Per trovare i sottotipi biometrici disponibili per un particolare tipo biometrico, usare la tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="274f8-113">To find the available biometric subtypes for a particular biometric type, use the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="274f8-114">Valore <strong>WINBIO_BIOMETRIC_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="274f8-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> value</span></span></th>
<th><span data-ttu-id="274f8-115">Argomenti per trovare i valori <strong>WINBIO_BIOMETRIC_SUBTYPE</strong></span><span class="sxs-lookup"><span data-stu-id="274f8-115">Topic(s) to find <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="274f8-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span><span class="sxs-lookup"><span data-stu-id="274f8-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span></span></td>
<td><span data-ttu-id="274f8-117"><a href="winbio-ansi-385-face-constants.md"><strong>Costanti WINBIO_ANSI_385_FACE</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="274f8-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="274f8-118">Questi valori si applicano solo a Windows 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="274f8-118">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="274f8-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span><span class="sxs-lookup"><span data-stu-id="274f8-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span></span></td>
<td><span data-ttu-id="274f8-120">Uno degli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="274f8-120">One of the following topics:</span></span>
<ul>
<li><span data-ttu-id="274f8-121"><a href="winbio-ansi-381-format-constants.md"><strong>Costanti WINBIO_ANSI_381_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="274f8-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT Constants</strong></a></span></span></li>
<li><span data-ttu-id="274f8-122"><a href="winbio-ansi-381-img-constants.md"><strong>Costanti WINBIO_ANSI_381_IMG</strong></a></span><span class="sxs-lookup"><span data-stu-id="274f8-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG Constants</strong></a></span></span></li>
<li><span data-ttu-id="274f8-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>Costanti WINBIO_ANSI_381_IMG_ACQ</strong></a></span><span class="sxs-lookup"><span data-stu-id="274f8-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ Constants</strong></a></span></span></li>
<li><span data-ttu-id="274f8-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>Costanti WINBIO_ANSI_381_IMP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="274f8-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE Constants</strong></a></span></span></li>
<li><span data-ttu-id="274f8-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>Costanti WINBIO_ANSI_381_PIXELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="274f8-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS Constants</strong></a></span></span></li>
<li><span data-ttu-id="274f8-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>Costanti impronta digitale WINBIO_ANSI_381_POS</strong></a></span><span class="sxs-lookup"><span data-stu-id="274f8-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerprint Constants</strong></a></span></span></li>
<li><span data-ttu-id="274f8-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>Costanti WINBIO_ANSI_381_POS_Palm</strong></a></span><span class="sxs-lookup"><span data-stu-id="274f8-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm Constants</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="274f8-128"><strong>WINBIO_TYPE_IRIS</strong></span><span class="sxs-lookup"><span data-stu-id="274f8-128"><strong>WINBIO_TYPE_IRIS</strong></span></span></td>
<td><span data-ttu-id="274f8-129"><a href="winbio-iris-constants.md"><strong>Costanti WINBIO_IRIS</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="274f8-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="274f8-130">Questi valori si applicano solo a Windows 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="274f8-130">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="274f8-131"><strong>WINBIO_TYPE_VOICE</strong></span><span class="sxs-lookup"><span data-stu-id="274f8-131"><strong>WINBIO_TYPE_VOICE</strong></span></span></td>
<td><span data-ttu-id="274f8-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>Costanti WINBIO_VOICE</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="274f8-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="274f8-133">Questi valori si applicano solo a Windows 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="274f8-133">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="274f8-134">Per ulteriori informazioni, vedere [costanti dell'applicazione client](client-application-constants.md).</span><span class="sxs-lookup"><span data-stu-id="274f8-134">For more information, see [Client Application Constants](client-application-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="274f8-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="274f8-135">Requirements</span></span>



| <span data-ttu-id="274f8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="274f8-136">Requirement</span></span> | <span data-ttu-id="274f8-137">Valore</span><span class="sxs-lookup"><span data-stu-id="274f8-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="274f8-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="274f8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="274f8-139">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="274f8-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="274f8-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="274f8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="274f8-141">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="274f8-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="274f8-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="274f8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="274f8-143"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="274f8-143"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





