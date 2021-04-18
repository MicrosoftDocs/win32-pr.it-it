---
title: Struttura WINBIO_STORAGE_SCHEMA ( \_ tipi WINBIO. h)
description: Descrive le funzionalità di un adattatore di archiviazione biometrico.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- Struttura di WINBIO_STORAGE_SCHEMA Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_STORAGE_SCHEMA
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302620"
---
# <a name="winbio_storage_schema-structure"></a><span data-ttu-id="87c0f-105">\_ \_ Struttura dello schema di archiviazione WINBIO</span><span class="sxs-lookup"><span data-stu-id="87c0f-105">WINBIO\_STORAGE\_SCHEMA structure</span></span>

<span data-ttu-id="87c0f-106">La **struttura \_ \_ dello schema di archiviazione WINBIO** descrive le funzionalità di un adattatore di archiviazione biometrico.</span><span class="sxs-lookup"><span data-stu-id="87c0f-106">The **WINBIO\_STORAGE\_SCHEMA** structure describes the capabilities of a biometric storage adapter.</span></span> <span data-ttu-id="87c0f-107">Questa struttura viene utilizzata dalla funzione [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) .</span><span class="sxs-lookup"><span data-stu-id="87c0f-107">This structure is used by the [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c0f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87c0f-108">Syntax</span></span>


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="87c0f-109">Members</span><span class="sxs-lookup"><span data-stu-id="87c0f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="87c0f-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="87c0f-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="87c0f-111">Tipo di misurazione biometrica salvata nel database.</span><span class="sxs-lookup"><span data-stu-id="87c0f-111">The type of biometric measurement saved in the database.</span></span>

</dd> <dt>

<span data-ttu-id="87c0f-112">**DatabaseId**</span><span class="sxs-lookup"><span data-stu-id="87c0f-112">**DatabaseId**</span></span>
</dt> <dd>

<span data-ttu-id="87c0f-113">GUID che identifica il database.</span><span class="sxs-lookup"><span data-stu-id="87c0f-113">A GUID that identifies the database.</span></span>

</dd> <dt>

<span data-ttu-id="87c0f-114">**DataFormat**</span><span class="sxs-lookup"><span data-stu-id="87c0f-114">**DataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="87c0f-115">GUID che identifica il formato dei modelli nel database.</span><span class="sxs-lookup"><span data-stu-id="87c0f-115">A GUID that identifies the format of the templates in the database.</span></span>

</dd> <dt>

<span data-ttu-id="87c0f-116">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="87c0f-116">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="87c0f-117">Informazioni sulle caratteristiche del database.</span><span class="sxs-lookup"><span data-stu-id="87c0f-117">Information about the characteristics of the database.</span></span> <span data-ttu-id="87c0f-118">Può trattarsi di un **or** bit per bit delle costanti seguenti.</span><span class="sxs-lookup"><span data-stu-id="87c0f-118">This can be a bitwise **OR** of the following constants.</span></span>



| <span data-ttu-id="87c0f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="87c0f-119">Value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="87c0f-120">Significato</span><span class="sxs-lookup"><span data-stu-id="87c0f-120">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="87c0f-121"><dt>**WINBIO \_ \_ \_ Maschera di flag del database**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="87c0f-121"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="87c0f-122">Rappresenta una maschera per i bit del flag.</span><span class="sxs-lookup"><span data-stu-id="87c0f-122">Represents a mask for the flag bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="87c0f-123"><dt>**WINBIO \_ FLAG di DATABASE 0x00020000 \_ \_ remoto**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87c0f-123"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="87c0f-124">Il database si trova in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="87c0f-124">The database resides on a remote computer.</span></span><br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="87c0f-125"><dt>**WINBIO \_ FLAG di DATABASE 0x00010000 \_ \_ rimovibile**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87c0f-125"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="87c0f-126">Il database risiede in un'unità rimovibile.</span><span class="sxs-lookup"><span data-stu-id="87c0f-126">The database resides on a removable drive.</span></span><br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="87c0f-127"><dt>**WINBIO \_ Tipo di DATABASE \_ \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="87c0f-127"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="87c0f-128">Il database è gestito da un sistema di gestione di database.</span><span class="sxs-lookup"><span data-stu-id="87c0f-128">The database is managed by a database management system.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="87c0f-129"><dt>**WINBIO \_ \_ \_ File di tipo database**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="87c0f-129"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="87c0f-130">Il database è contenuto in un file.</span><span class="sxs-lookup"><span data-stu-id="87c0f-130">The database is contained in a file.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="87c0f-131"><dt>**WINBIO \_ \_ \_ Maschera del tipo di database**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="87c0f-131"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="87c0f-132">Rappresenta una maschera per i bit del tipo.</span><span class="sxs-lookup"><span data-stu-id="87c0f-132">Represents a mask for the type bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="87c0f-133"><dt>**WINBIO \_ Tipo di DATABASE \_ \_ OnChip**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="87c0f-133"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="87c0f-134">Il database risiede nel sensore biometrico.</span><span class="sxs-lookup"><span data-stu-id="87c0f-134">The database resides on the biometric sensor.</span></span><br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="87c0f-135"><dt>**WINBIO \_ Tipo di DATABASE \_ \_ smartcard**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="87c0f-135"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="87c0f-136">Il database risiede in una smart card.</span><span class="sxs-lookup"><span data-stu-id="87c0f-136">The database resides on a smart card.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="87c0f-137">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="87c0f-137">**FilePath**</span></span>
</dt> <dd>

<span data-ttu-id="87c0f-138">Il percorso e il nome file del database se si trova sul disco del computer.</span><span class="sxs-lookup"><span data-stu-id="87c0f-138">The path and file name of the database if it resides on the computer disk.</span></span>

</dd> <dt>

<span data-ttu-id="87c0f-139">**ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="87c0f-139">**ConnectionString**</span></span>
</dt> <dd>

<span data-ttu-id="87c0f-140">Valore stringa che può essere inviato a un server di database per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="87c0f-140">A string value that can be sent to a database server to identify the database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87c0f-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87c0f-141">Requirements</span></span>



| <span data-ttu-id="87c0f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="87c0f-142">Requirement</span></span> | <span data-ttu-id="87c0f-143">Valore</span><span class="sxs-lookup"><span data-stu-id="87c0f-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87c0f-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87c0f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="87c0f-145">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="87c0f-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="87c0f-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87c0f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="87c0f-147">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="87c0f-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="87c0f-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87c0f-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="87c0f-149"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87c0f-149"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87c0f-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87c0f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c0f-151">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="87c0f-151">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="87c0f-152">**WinBioEnumDatabases**</span><span class="sxs-lookup"><span data-stu-id="87c0f-152">**WinBioEnumDatabases**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





