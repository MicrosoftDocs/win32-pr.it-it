---
title: Costanti WINBIO_FLAG (tipi WinBio \_ . h)
description: Specificare la configurazione dell'unità biometrica e le caratteristiche di accesso per la nuova sessione.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400352"
---
# <a name="winbio_flag-constants"></a><span data-ttu-id="bf636-103">\_Costanti flag WINBIO</span><span class="sxs-lookup"><span data-stu-id="bf636-103">WINBIO\_FLAG Constants</span></span>

<span data-ttu-id="bf636-104">Nella funzione [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) è possibile usare le costanti seguenti per specificare la configurazione di unità biometriche e le caratteristiche di accesso per la nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="bf636-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify biometric unit configuration and access characteristics for the new session.</span></span>



| <span data-ttu-id="bf636-105">Costante</span><span class="sxs-lookup"><span data-stu-id="bf636-105">Constant</span></span>                                                                                                                                                                                     | <span data-ttu-id="bf636-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf636-106">Description</span></span>                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <span data-ttu-id="bf636-107"><dt>**\_impostazione predefinita del flag WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bf636-107"><dt>**WINBIO\_FLAG\_DEFAULT**</dt></span></span> </dl>             | <span data-ttu-id="bf636-108">Flag di configurazione del sensore.</span><span class="sxs-lookup"><span data-stu-id="bf636-108">Sensor configuration flag.</span></span> <span data-ttu-id="bf636-109">Le unità biometriche operano nel modo specificato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="bf636-109">The biometric units operate in the manner specified during installation.</span></span><br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <span data-ttu-id="bf636-110"><dt>**\_flag WINBIO \_ Basic**</dt></span><span class="sxs-lookup"><span data-stu-id="bf636-110"><dt>**WINBIO\_FLAG\_BASIC**</dt></span></span> </dl>                   | <span data-ttu-id="bf636-111">Flag di configurazione del sensore.</span><span class="sxs-lookup"><span data-stu-id="bf636-111">Sensor configuration flag.</span></span> <span data-ttu-id="bf636-112">Le unità biometriche funzionano solo come dispositivi di acquisizione di base.</span><span class="sxs-lookup"><span data-stu-id="bf636-112">The biometric units operate only as basic capture devices.</span></span><br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <span data-ttu-id="bf636-113"><dt>**\_flag WINBIO \_ avanzato**</dt></span><span class="sxs-lookup"><span data-stu-id="bf636-113"><dt>**WINBIO\_FLAG\_ADVANCED**</dt></span></span> </dl>          | <span data-ttu-id="bf636-114">Flag di configurazione del sensore.</span><span class="sxs-lookup"><span data-stu-id="bf636-114">Sensor configuration flag.</span></span> <span data-ttu-id="bf636-115">Le unità biometriche usano le funzionalità di elaborazione e archiviazione interne.</span><span class="sxs-lookup"><span data-stu-id="bf636-115">The biometric units use internal processing and storage capabilities.</span></span><br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <span data-ttu-id="bf636-116"><dt>**FLAG WINBIO non \_ \_ elaborato**</dt></span><span class="sxs-lookup"><span data-stu-id="bf636-116"><dt>**WINBIO\_FLAG\_RAW**</dt></span></span> </dl>                         | <span data-ttu-id="bf636-117">Flag di accesso desiderato.</span><span class="sxs-lookup"><span data-stu-id="bf636-117">Desired access flag.</span></span> <span data-ttu-id="bf636-118">L'applicazione client acquisisce i dati biometrici non elaborati usando [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="bf636-118">The client application captures raw biometric data using [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span><br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <span data-ttu-id="bf636-119"><dt>**\_manutenzione del flag WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bf636-119"><dt>**WINBIO\_FLAG\_MAINTENANCE**</dt></span></span> </dl> | <span data-ttu-id="bf636-120">Flag di accesso desiderato.</span><span class="sxs-lookup"><span data-stu-id="bf636-120">Desired access flag.</span></span> <span data-ttu-id="bf636-121">Il client esegue operazioni di controllo definite dal fornitore su un'unità biometrica chiamando [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="bf636-121">The client performs vendor-defined control operations on a biometric unit by calling [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bf636-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf636-122">Requirements</span></span>



| <span data-ttu-id="bf636-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf636-123">Requirement</span></span> | <span data-ttu-id="bf636-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bf636-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf636-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf636-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bf636-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bf636-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="bf636-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf636-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bf636-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf636-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bf636-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf636-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf636-130"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf636-130"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf636-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf636-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf636-132">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="bf636-132">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





