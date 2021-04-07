---
title: Costanti generali (tipi WinBio \_ . h)
description: Specificare lunghezza massima SID, handle, ID, lunghezza massima della stringa e dimensioni massime del buffer di esempio.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964217"
---
# <a name="general-constants-winbio_typesh"></a><span data-ttu-id="b148b-103">Costanti generali (tipi WinBio \_ . h)</span><span class="sxs-lookup"><span data-stu-id="b148b-103">General Constants (Winbio\_types.h)</span></span>

<span data-ttu-id="b148b-104">In Windows Biometric Framework vengono utilizzate le costanti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b148b-104">The following constants are used throughout the Windows Biometric Framework.</span></span>



| <span data-ttu-id="b148b-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b148b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="b148b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b148b-106">Description</span></span>                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <span data-ttu-id="b148b-107"><dt>**\_dimensioni massime \_ SID sicurezza \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b148b-107"><dt>**SECURITY\_MAX\_SID\_SIZE**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="b148b-108">Lunghezza massima del valore di un ID di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="b148b-108">The maximum length of a security identifier (SID) value.</span></span> <span data-ttu-id="b148b-109">Attualmente è 68.</span><span class="sxs-lookup"><span data-stu-id="b148b-109">Currently this is 68.</span></span><br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <span data-ttu-id="b148b-110"><dt>**\_ID unità \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="b148b-110"><dt>**WINBIO\_UNIT\_ID**</dt></span></span> </dl>                                                                                                                | <span data-ttu-id="b148b-111">ID del numero di unità biometriche.</span><span class="sxs-lookup"><span data-stu-id="b148b-111">ID number of a biometric unit.</span></span><br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <span data-ttu-id="b148b-112"><dt>**\_handle della sessione WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b148b-112"><dt>**WINBIO\_SESSION\_HANDLE**</dt></span></span> </dl>                                                                                           | <span data-ttu-id="b148b-113">Un long integer senza segno contenente l'handle per una sessione biometrica aperta.</span><span class="sxs-lookup"><span data-stu-id="b148b-113">An unsigned long integer that contains the handle for an open biometric session.</span></span><br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <span data-ttu-id="b148b-114"><dt>**\_handle WINBIO Framework \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b148b-114"><dt>**WINBIO\_FRAMEWORK\_HANDLE**</dt></span></span> </dl>                                                                                     | <span data-ttu-id="b148b-115">Valore long integer senza segno contenente l'handle per una sessione di Framework aperta.</span><span class="sxs-lookup"><span data-stu-id="b148b-115">An unsigned long integer that contains the handle for an open framework session.</span></span><br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <span data-ttu-id="b148b-116"><dt>**\_UUID WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="b148b-116"><dt>**WINBIO\_UUID**</dt></span></span> </dl>                                                                                                                          | <span data-ttu-id="b148b-117">Un valore GUID.</span><span class="sxs-lookup"><span data-stu-id="b148b-117">A GUID.</span></span><br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <span data-ttu-id="b148b-118"><dt>**\_stringa WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="b148b-118"><dt>**WINBIO\_STRING**</dt></span></span> </dl>                                                                                                                    | <span data-ttu-id="b148b-119">Matrice di byte che contiene una stringa Unicode con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="b148b-119">A byte array that contains a null-terminated Unicode string.</span></span><br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <span data-ttu-id="b148b-120"><dt>**WINBIO \_ \_ \_ lunghezza massima stringa**</dt></span><span class="sxs-lookup"><span data-stu-id="b148b-120"><dt>**WINBIO\_MAX\_STRING\_LEN** </dt></span></span> </dl>                                                                                       | <span data-ttu-id="b148b-121">Lunghezza massima di un valore **\_ stringa WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="b148b-121">The maximum length of a **WINBIO\_STRING** value.</span></span> <span data-ttu-id="b148b-122">Attualmente è 256.</span><span class="sxs-lookup"><span data-stu-id="b148b-122">Currently this is 256.</span></span><br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <span data-ttu-id="b148b-123"><dt>**WINBIO \_ \_ \_ \_ Dimensioni massime del buffer di esempio**</dt> <dt>0x7FFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="b148b-123"><dt>**WINBIO\_MAX\_SAMPLE\_BUFFER\_SIZE**</dt> <dt>0x7FFFFFFF</dt></span></span> </dl> | <span data-ttu-id="b148b-124">Il numero massimo di byte in una singola acquisizione di dati biometrici.</span><span class="sxs-lookup"><span data-stu-id="b148b-124">The maximum number of bytes in a single biometric data capture.</span></span><br/>                  |



## <a name="requirements"></a><span data-ttu-id="b148b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b148b-125">Requirements</span></span>



| <span data-ttu-id="b148b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b148b-126">Requirement</span></span> | <span data-ttu-id="b148b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b148b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b148b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b148b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b148b-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b148b-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="b148b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b148b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b148b-131">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b148b-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b148b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b148b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b148b-133"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b148b-133"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b148b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b148b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b148b-135">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="b148b-135">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





