---
title: Costanti WINBIO_SETTING_SOURCE (tipi WinBio \_ . h)
description: Determinare se la Windows Biometric Framework è attualmente abilitata.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964908"
---
# <a name="winbio_setting_source-constants"></a><span data-ttu-id="e2448-103">Costanti di origine dell' \_ impostazione WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="e2448-103">WINBIO\_SETTING\_SOURCE Constants</span></span>

<span data-ttu-id="e2448-104">Le costanti seguenti vengono usate dalla funzione [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) per determinare se la Windows Biometric Framework è attualmente abilitata.</span><span class="sxs-lookup"><span data-stu-id="e2448-104">The following constants are used by the [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) function to determine whether the Windows Biometric Framework is currently enabled.</span></span> <span data-ttu-id="e2448-105">Le costanti specificano la posizione in cui ha avuto origine l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="e2448-105">The constants specify where the setting originated.</span></span>



| <span data-ttu-id="e2448-106">Costante</span><span class="sxs-lookup"><span data-stu-id="e2448-106">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="e2448-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2448-107">Description</span></span>                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <span data-ttu-id="e2448-108"><dt>**\_origine impostazione \_ WINBIO \_ non valida**</dt></span><span class="sxs-lookup"><span data-stu-id="e2448-108"><dt>**WINBIO\_SETTING\_SOURCE\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="e2448-109">Impostazione non valida.</span><span class="sxs-lookup"><span data-stu-id="e2448-109">The setting is not valid.</span></span><br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <span data-ttu-id="e2448-110"><dt>**\_impostazione \_ predefinita di origine dell'impostazione WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2448-110"><dt>**WINBIO\_SETTING\_SOURCE\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="e2448-111">L'impostazione è stata originata dai criteri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="e2448-111">The setting originated from built-in policy.</span></span><br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <span data-ttu-id="e2448-112"><dt>**\_criteri di \_ origine \_ impostazione WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="e2448-112"><dt>**WINBIO\_SETTING\_SOURCE\_POLICY**</dt></span></span> </dl>    | <span data-ttu-id="e2448-113">L'impostazione è stata originata nel registro di sistema del computer locale.</span><span class="sxs-lookup"><span data-stu-id="e2448-113">The setting originated in the local computer registry.</span></span><br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <span data-ttu-id="e2448-114"><dt>**WINBIO \_ impostazione \_ origine \_ locale**</dt></span><span class="sxs-lookup"><span data-stu-id="e2448-114"><dt>**WINBIO\_SETTING\_SOURCE\_LOCAL**</dt></span></span> </dl>       | <span data-ttu-id="e2448-115">L'impostazione è stata creata da Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="e2448-115">The setting was created by Group Policy</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="e2448-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2448-116">Requirements</span></span>



| <span data-ttu-id="e2448-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2448-117">Requirement</span></span> | <span data-ttu-id="e2448-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e2448-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2448-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2448-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2448-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e2448-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e2448-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2448-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2448-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2448-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e2448-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2448-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2448-124"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2448-124"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2448-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2448-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2448-126">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="e2448-126">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





