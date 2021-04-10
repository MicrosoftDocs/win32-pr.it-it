---
title: Costanti WINBIO_DB (tipi WinBio \_ . h)
description: Specificare il database da utilizzare per un pool di sistema.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120230"
---
# <a name="winbio_db-constants"></a><span data-ttu-id="ae7b7-103">\_Costanti database WINBIO</span><span class="sxs-lookup"><span data-stu-id="ae7b7-103">WINBIO\_DB Constants</span></span>

<span data-ttu-id="ae7b7-104">Quando si chiama [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) per specificare il database da utilizzare per un pool di sistema, è possibile utilizzare le costanti seguenti.</span><span class="sxs-lookup"><span data-stu-id="ae7b7-104">The following constants can be used when calling [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to specify the database to be used for a system pool.</span></span>



| <span data-ttu-id="ae7b7-105">Costante</span><span class="sxs-lookup"><span data-stu-id="ae7b7-105">Constant</span></span>                                                                                                                                                                         | <span data-ttu-id="ae7b7-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae7b7-106">Description</span></span>                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <span data-ttu-id="ae7b7-107"><dt>**\_ \_ impostazione predefinita database WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="ae7b7-107"><dt>**WINBIO\_DB\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="ae7b7-108">Ogni unità biometrica nel pool di sensori usa il database predefinito specificato nella configurazione predefinita dell'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="ae7b7-108">Each biometric unit in the sensor pool uses the default database specified in the default biometric unit configuration.</span></span><br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <span data-ttu-id="ae7b7-109"><dt>**\_bootstrap del database WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ae7b7-109"><dt>**WINBIO\_DB\_BOOTSTRAP**</dt></span></span> </dl> | <span data-ttu-id="ae7b7-110">Può essere usato per gli scenari prima dell'avvio di Windows.</span><span class="sxs-lookup"><span data-stu-id="ae7b7-110">Can be used for scenarios prior to starting Windows.</span></span> <span data-ttu-id="ae7b7-111">In genere, il database fa parte del chip del sensore o fa parte del BIOS e può essere usato solo per la registrazione e l'eliminazione del modello.</span><span class="sxs-lookup"><span data-stu-id="ae7b7-111">Typically, the database is part of the sensor chip or is part of the BIOS and can only be used for template enrollment and deletion.</span></span><br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <span data-ttu-id="ae7b7-112"><dt>**WINBIO \_ database \_ OnChip**</dt></span><span class="sxs-lookup"><span data-stu-id="ae7b7-112"><dt>**WINBIO\_DB\_ONCHIP**</dt></span></span> </dl>          | <span data-ttu-id="ae7b7-113">Il database si trova sul chip del sensore.</span><span class="sxs-lookup"><span data-stu-id="ae7b7-113">The database resides on the sensor chip.</span></span><br/>                                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="ae7b7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae7b7-114">Requirements</span></span>



| <span data-ttu-id="ae7b7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae7b7-115">Requirement</span></span> | <span data-ttu-id="ae7b7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ae7b7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7b7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae7b7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ae7b7-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ae7b7-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="ae7b7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae7b7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ae7b7-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae7b7-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ae7b7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae7b7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae7b7-122"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae7b7-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae7b7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae7b7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae7b7-124">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="ae7b7-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





