---
title: Costanti WINBIO_DATABASE_TYPE (tipi WinBio \_ . h)
description: Flag che possono essere utilizzati per il membro Attributes della \_ \_ struttura dello schema di archiviazione WINBIO.
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741527"
---
# <a name="winbio_database_type-constants"></a><span data-ttu-id="39550-103">Costanti del tipo di \_ database WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="39550-103">WINBIO\_DATABASE\_TYPE Constants</span></span>

<span data-ttu-id="39550-104">I flag seguenti possono essere usati per il membro **Attributes** della [**struttura \_ \_ dello schema di archiviazione WINBIO**](winbio-storage-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="39550-104">The following flags can be used for the **Attributes** member of the [**WINBIO\_STORAGE\_SCHEMA**](winbio-storage-schema.md) structure.</span></span>



| <span data-ttu-id="39550-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="39550-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="39550-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39550-106">Description</span></span>                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="39550-107"><dt>**WINBIO \_ \_ \_ Maschera del tipo di database**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="39550-107"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="39550-108">Rappresenta una maschera per tutti i \_ bit di tipo \_ .</span><span class="sxs-lookup"><span data-stu-id="39550-108">Represents a mask for all of the \_TYPE\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="39550-109"><dt>**WINBIO \_ \_ \_ File di tipo database**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="39550-109"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="39550-110">Il database è contenuto in un file.</span><span class="sxs-lookup"><span data-stu-id="39550-110">The database is contained in a file.</span></span><br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="39550-111"><dt>**WINBIO \_ Tipo di DATABASE \_ \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="39550-111"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="39550-112">Il database è gestito da un componente del sistema di gestione di database (DBMS) esterno, ad esempio Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="39550-112">The database is managed by an external database management system (DBMS) component, such as Microsoft SQL Server.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="39550-113"><dt>**WINBIO \_ Tipo di DATABASE \_ \_ OnChip**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="39550-113"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="39550-114">Il database risiede nel sensore biometrico.</span><span class="sxs-lookup"><span data-stu-id="39550-114">The database resides on the biometric sensor.</span></span><br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="39550-115"><dt>**WINBIO \_ Tipo di DATABASE \_ \_ smartcard**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="39550-115"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="39550-116">Il database risiede in una smart card.</span><span class="sxs-lookup"><span data-stu-id="39550-116">The database resides on a smart card.</span></span><br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="39550-117"><dt>**WINBIO \_ \_ \_ Maschera di flag del database**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="39550-117"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="39550-118">Rappresenta una maschera per tutti i \_ bit del flag \_ .</span><span class="sxs-lookup"><span data-stu-id="39550-118">Represents a mask for all of the \_FLAG\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="39550-119"><dt>**WINBIO \_ FLAG di DATABASE 0x00010000 \_ \_ rimovibile**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="39550-119"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="39550-120">Il supporto di archiviazione che contiene il database può essere rimosso fisicamente dal computer.</span><span class="sxs-lookup"><span data-stu-id="39550-120">The storage medium containing the database can be physically removed from the computer.</span></span><br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="39550-121"><dt>**WINBIO \_ FLAG di DATABASE 0x00020000 \_ \_ remoto**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="39550-121"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="39550-122">Il database si trova in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="39550-122">The database resides on a remote computer.</span></span><br/>                                                                        |



## <a name="requirements"></a><span data-ttu-id="39550-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39550-123">Requirements</span></span>



| <span data-ttu-id="39550-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="39550-124">Requirement</span></span> | <span data-ttu-id="39550-125">Valore</span><span class="sxs-lookup"><span data-stu-id="39550-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39550-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39550-126">Minimum supported client</span></span><br/> | <span data-ttu-id="39550-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="39550-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="39550-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39550-128">Minimum supported server</span></span><br/> | <span data-ttu-id="39550-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="39550-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="39550-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39550-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="39550-131"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39550-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39550-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39550-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39550-133">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="39550-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





