---
title: Struttura WINBIO_IDENTITY ( \_ tipi WINBIO. h)
description: Contiene un valore di identificazione associato a un modello biometrico.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- Struttura di WINBIO_IDENTITY Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119982"
---
# <a name="winbio_identity-structure"></a><span data-ttu-id="093c8-104">\_Struttura di identità WINBIO</span><span class="sxs-lookup"><span data-stu-id="093c8-104">WINBIO\_IDENTITY structure</span></span>

<span data-ttu-id="093c8-105">La struttura di **\_ identità WINBIO** contiene un valore di identificazione associato a un modello biometrico.</span><span class="sxs-lookup"><span data-stu-id="093c8-105">The **WINBIO\_IDENTITY** structure contains an identifying value associated with a biometric template.</span></span>

## <a name="syntax"></a><span data-ttu-id="093c8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="093c8-106">Syntax</span></span>


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a><span data-ttu-id="093c8-107">Members</span><span class="sxs-lookup"><span data-stu-id="093c8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="093c8-108">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="093c8-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="093c8-109">Specifica il formato delle informazioni di identità contenute nella struttura.</span><span class="sxs-lookup"><span data-stu-id="093c8-109">Specifies the format of the identity information contained in this structure.</span></span> <span data-ttu-id="093c8-110">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="093c8-110">This can be one of the following values:</span></span>



| <span data-ttu-id="093c8-111">Valore</span><span class="sxs-lookup"><span data-stu-id="093c8-111">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="093c8-112">Significato</span><span class="sxs-lookup"><span data-stu-id="093c8-112">Meaning</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="093c8-113"><dt>**\_tipo di ID WINBIO \_ \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="093c8-113"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="093c8-114">Al modello non è associato alcun ID.</span><span class="sxs-lookup"><span data-stu-id="093c8-114">The template has no associated ID.</span></span><br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="093c8-115"><dt>**\_ \_ carattere jolly tipo ID WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="093c8-115"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="093c8-116">La struttura corrisponde a tutte le identità del modello.</span><span class="sxs-lookup"><span data-stu-id="093c8-116">The structure matches all template identities.</span></span><br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="093c8-117"><dt>**\_ \_ GUID tipo ID \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="093c8-117"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="093c8-118">La struttura contiene un GUID associato al modello.</span><span class="sxs-lookup"><span data-stu-id="093c8-118">The structure contains a GUID associated with the template.</span></span><br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="093c8-119"><dt>**\_ \_ SID tipo ID \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="093c8-119"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="093c8-120">La struttura contiene il SID dell'account associato al modello.</span><span class="sxs-lookup"><span data-stu-id="093c8-120">The structure contains the account SID associated with the template.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="093c8-121">**Valore**</span><span class="sxs-lookup"><span data-stu-id="093c8-121">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="093c8-122">Unione che può contenere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="093c8-122">A union that can contain one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="093c8-123">**Null**</span><span class="sxs-lookup"><span data-stu-id="093c8-123">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="093c8-124">Contiene 1 se il membro del **tipo** è **WINBIO \_ ID \_ tipo \_ null**.</span><span class="sxs-lookup"><span data-stu-id="093c8-124">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="093c8-125">**Jolly**</span><span class="sxs-lookup"><span data-stu-id="093c8-125">**Wildcard**</span></span>
</dt> <dd>

<span data-ttu-id="093c8-126">Contiene 1 se il membro del **tipo** è un **\_ \_ \_ carattere jolly di tipo ID WINBIO**.</span><span class="sxs-lookup"><span data-stu-id="093c8-126">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_WILDCARD**.</span></span>

</dd> <dt>

<span data-ttu-id="093c8-127">**TemplateGuid**</span><span class="sxs-lookup"><span data-stu-id="093c8-127">**TemplateGuid**</span></span>
</dt> <dd>

<span data-ttu-id="093c8-128">Contiene un valore GUID a 128 bit che identifica il modello se il membro del **tipo** è **WINBIO \_ ID \_ tipo \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="093c8-128">Contains a 128-bit GUID value that identifies the template if the **Type** member is **WINBIO\_ID\_TYPE\_GUID**.</span></span>

</dd> <dt>

<span data-ttu-id="093c8-129">**AccountSid**</span><span class="sxs-lookup"><span data-stu-id="093c8-129">**AccountSid**</span></span>
</dt> <dd>

<span data-ttu-id="093c8-130">Struttura che contiene un SID dell'account se il membro di **tipo** è **WINBIO \_ ID \_ tipo \_ SID**.</span><span class="sxs-lookup"><span data-stu-id="093c8-130">A structure that contains an account SID if the **Type** member is **WINBIO\_ID\_TYPE\_SID**.</span></span>

<dl> <dt>

<span data-ttu-id="093c8-131">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="093c8-131">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="093c8-132">Numero di caratteri nel SID.</span><span class="sxs-lookup"><span data-stu-id="093c8-132">The number of characters in the SID.</span></span>

</dd> <dt>

<span data-ttu-id="093c8-133">**Dati**</span><span class="sxs-lookup"><span data-stu-id="093c8-133">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="093c8-134">Matrice di caratteri non firmati che contengono il SID.</span><span class="sxs-lookup"><span data-stu-id="093c8-134">An array of unsigned characters that contain the SID.</span></span> <span data-ttu-id="093c8-135">La dimensione massima corrente della matrice è 68 caratteri.</span><span class="sxs-lookup"><span data-stu-id="093c8-135">The current maximum size of the array is 68 characters.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="093c8-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="093c8-136">Remarks</span></span>

<span data-ttu-id="093c8-137">Questa struttura viene utilizzata nelle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="093c8-137">This structure is used in the following functions:</span></span>

-   [<span data-ttu-id="093c8-138">**WinBioDeleteTemplate**</span><span class="sxs-lookup"><span data-stu-id="093c8-138">**WinBioDeleteTemplate**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [<span data-ttu-id="093c8-139">**WinBioEnrollCommit**</span><span class="sxs-lookup"><span data-stu-id="093c8-139">**WinBioEnrollCommit**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [<span data-ttu-id="093c8-140">**WinBioEnumEnrollments**</span><span class="sxs-lookup"><span data-stu-id="093c8-140">**WinBioEnumEnrollments**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [<span data-ttu-id="093c8-141">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="093c8-141">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [<span data-ttu-id="093c8-142">**WinBioIdentify**</span><span class="sxs-lookup"><span data-stu-id="093c8-142">**WinBioIdentify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [<span data-ttu-id="093c8-143">**WinBioRemoveCredential**</span><span class="sxs-lookup"><span data-stu-id="093c8-143">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [<span data-ttu-id="093c8-144">**WinBioVerify**</span><span class="sxs-lookup"><span data-stu-id="093c8-144">**WinBioVerify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [<span data-ttu-id="093c8-145">**WinBioVerifyWithCallback**</span><span class="sxs-lookup"><span data-stu-id="093c8-145">**WinBioVerifyWithCallback**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a><span data-ttu-id="093c8-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="093c8-146">Requirements</span></span>



| <span data-ttu-id="093c8-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="093c8-147">Requirement</span></span> | <span data-ttu-id="093c8-148">Valore</span><span class="sxs-lookup"><span data-stu-id="093c8-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="093c8-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="093c8-149">Minimum supported client</span></span><br/> | <span data-ttu-id="093c8-150">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="093c8-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="093c8-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="093c8-151">Minimum supported server</span></span><br/> | <span data-ttu-id="093c8-152">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="093c8-152">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="093c8-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="093c8-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="093c8-154"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="093c8-154"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="093c8-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="093c8-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="093c8-156">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="093c8-156">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





