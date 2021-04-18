---
description: Indica un MCA, un controllo del computer corretto (CMC) o una voce di informazioni di errore della piattaforma (CPE) corretta. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: Classe MSMCAInfo_Entry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316591"
---
# <a name="msmcainfo_entry-class"></a><span data-ttu-id="5836a-104">\_Classe entry MSMCAInfo</span><span class="sxs-lookup"><span data-stu-id="5836a-104">MSMCAInfo\_Entry class</span></span>

<span data-ttu-id="5836a-105">La classe di **\_ immissione MSMCAInfo** indica un MCA, un controllo del computer corretto (CMC) o una voce di informazioni di errore della piattaforma (CPE) corretta.</span><span class="sxs-lookup"><span data-stu-id="5836a-105">The **MSMCAInfo\_Entry** class indicates an MCA, corrected machine check (CMC), or corrected platform error (CPE) information entry.</span></span> <span data-ttu-id="5836a-106">Questa classe è disponibile solo nei sistemi Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="5836a-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="5836a-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5836a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5836a-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5836a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5836a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5836a-109">Syntax</span></span>

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a><span data-ttu-id="5836a-110">Members</span><span class="sxs-lookup"><span data-stu-id="5836a-110">Members</span></span>

<span data-ttu-id="5836a-111">La **classe \_ entry MSMCAInfo** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5836a-111">The **MSMCAInfo\_Entry** class has these types of members:</span></span>

-   [<span data-ttu-id="5836a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5836a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5836a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5836a-113">Properties</span></span>

<span data-ttu-id="5836a-114">La **classe \_ entry di MSMCAInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5836a-114">The **MSMCAInfo\_Entry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5836a-115">**Dati**</span><span class="sxs-lookup"><span data-stu-id="5836a-115">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5836a-116">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5836a-116">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5836a-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5836a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5836a-118">Matrice di interi che contiene un record di errore MCA completo come riportato da System Abstraction Layer (SAL).</span><span class="sxs-lookup"><span data-stu-id="5836a-118">Integer array that contains a complete MCA error record as reported by the system abstraction layer (SAL).</span></span> <span data-ttu-id="5836a-119">SAL è il codice bruciato in ROM che il sistema operativo chiama per eseguire operazioni dipendenti dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="5836a-119">The SAL is code burned into ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="5836a-120">È simile al BIOS su una piattaforma x86.</span><span class="sxs-lookup"><span data-stu-id="5836a-120">It is similar to the BIOS on an x86 platform.</span></span>

</dd> <dt>

<span data-ttu-id="5836a-121">**Length**</span><span class="sxs-lookup"><span data-stu-id="5836a-121">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5836a-122">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5836a-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5836a-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5836a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5836a-124">Numero di byte nel record di errore.</span><span class="sxs-lookup"><span data-stu-id="5836a-124">Number of bytes in the error record.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5836a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="5836a-125">Remarks</span></span>

<span data-ttu-id="5836a-126">La **classe \_ entry MSMCAInfo** deriva da [**MSMCAInfo**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="5836a-126">The **MSMCAInfo\_Entry** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5836a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5836a-127">Requirements</span></span>



| <span data-ttu-id="5836a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5836a-128">Requirement</span></span> | <span data-ttu-id="5836a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="5836a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5836a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5836a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5836a-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5836a-131">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="5836a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5836a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5836a-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5836a-133">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="5836a-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5836a-134">Namespace</span></span><br/>                | <span data-ttu-id="5836a-135">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="5836a-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="5836a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5836a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5836a-137"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5836a-137"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="5836a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5836a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5836a-139"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5836a-139"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5836a-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5836a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5836a-141">Classi MSMCA</span><span class="sxs-lookup"><span data-stu-id="5836a-141">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="5836a-142">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="5836a-142">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

 




