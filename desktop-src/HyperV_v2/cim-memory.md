---
description: Rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: Classe CIM_Memory (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529503"
---
# <a name="cim_memory-class-hyper-v-management"></a><span data-ttu-id="7ead9-103">Classe CIM_Memory (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="7ead9-103">CIM_Memory class (Hyper-V management)</span></span>

<span data-ttu-id="7ead9-104">Rappresenta le funzionalità e la gestione dei dispositivi logici correlati alla memoria.</span><span class="sxs-lookup"><span data-stu-id="7ead9-104">Represents the capabilities and management of memory-related logical devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ead9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ead9-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="7ead9-106">Members</span><span class="sxs-lookup"><span data-stu-id="7ead9-106">Members</span></span>

<span data-ttu-id="7ead9-107">La classe **CIM \_ Memory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7ead9-107">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="7ead9-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ead9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ead9-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ead9-109">Properties</span></span>

<span data-ttu-id="7ead9-110">La classe di **\_ memoria CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7ead9-110">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ead9-111">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="7ead9-111">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-112">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7ead9-112">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-114">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,18 "," MIF. DMTF \| matrice di memoria fisica \| 001,13 ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-114">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.18", "MIF.DMTF\|Physical Memory Array\|001.13")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-115">Matrice di ottetti che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="7ead9-115">An array of octets that contains additional error information.</span></span> <span data-ttu-id="7ead9-116">Un esempio è la sindrome ECC o il ritorno dei bit di controllo se viene usata una metodologia di errore basata su CRC.</span><span class="sxs-lookup"><span data-stu-id="7ead9-116">An example is ECC syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="7ead9-117">Nel secondo caso, se viene riconosciuto un errore di bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7ead9-117">In the latter case, if a single bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span>

<span data-ttu-id="7ead9-118">Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7ead9-118">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-119">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="7ead9-119">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ead9-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-122">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-123">**true** se l'errore più recente è correggibile. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7ead9-123">**true** if the most recent error is correctable; otherwise, **false**.</span></span> <span data-ttu-id="7ead9-124">Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7ead9-124">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="7ead9-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ead9-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-128">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,4 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,5 "), **punito** (" byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-129">Indirizzo finale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per l'oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="7ead9-129">The ending address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="7ead9-130">L'indirizzo finale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="7ead9-130">The ending address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-131">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="7ead9-131">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-132">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ead9-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-134">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-134">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-135">Operazione di accesso alla memoria che ha causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="7ead9-135">The memory access operation that caused the last error.</span></span> <span data-ttu-id="7ead9-136">Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7ead9-136">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7ead9-137">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7ead9-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ead9-138">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="7ead9-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="7ead9-139">**Lettura** (3)</span><span class="sxs-lookup"><span data-stu-id="7ead9-139">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="7ead9-140">**Scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="7ead9-140">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="7ead9-141">**Scrittura parziale** (5)</span><span class="sxs-lookup"><span data-stu-id="7ead9-141">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ead9-142">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="7ead9-142">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-143">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ead9-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-145">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. IndirizzoIniziale"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,19 "," MIF. DMTF \| matrice di memoria fisica \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-145">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.19", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-146">Indirizzo dell'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="7ead9-146">The address of the last memory error.</span></span> <span data-ttu-id="7ead9-147">Il tipo di errore è descritto dalla proprietà **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="7ead9-147">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="7ead9-148">Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7ead9-148">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-149">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="7ead9-149">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-150">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7ead9-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-152">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorData"), **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,12 ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-152">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorData"), **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.12")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-153">Matrice che contiene i dati acquisiti durante l'ultimo accesso errato alla memoria.</span><span class="sxs-lookup"><span data-stu-id="7ead9-153">An array that contains data captured during the last erroneous memory access.</span></span> <span data-ttu-id="7ead9-154">I dati occupano i primi n ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="7ead9-154">The data occupies the first n octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span>

<span data-ttu-id="7ead9-155">Se la proprietà **ErrorTransferSize** contiene "0" (OK), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7ead9-155">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-156">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="7ead9-156">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-157">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ead9-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-159">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorDataOrder")</span><span class="sxs-lookup"><span data-stu-id="7ead9-159">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorDataOrder")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-160">Ordinamento dei dati archiviati nella proprietà **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="7ead9-160">The ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="7ead9-161">È possibile specificare "byte meno significativo per primo" (valore = 1) o "primo byte significativo" (2).</span><span class="sxs-lookup"><span data-stu-id="7ead9-161">"Least Significant Byte First" (value=1) or "Most Significant Byte First" (2) can be specified.</span></span> <span data-ttu-id="7ead9-162">Se la proprietà **ErrorTransferSize** contiene "0" (OK), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7ead9-162">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ead9-163">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7ead9-163">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="7ead9-164">**Byte meno significativi prima** (1)</span><span class="sxs-lookup"><span data-stu-id="7ead9-164">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="7ead9-165">**Primo byte significativo** (2)</span><span class="sxs-lookup"><span data-stu-id="7ead9-165">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ead9-166">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="7ead9-166">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ead9-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-169">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,12 "," MIF. \|Matrice di memoria fisica DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="7ead9-169">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-170">Tipo dell'ultimo errore che si verifica.</span><span class="sxs-lookup"><span data-stu-id="7ead9-170">The type of the last error to occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7ead9-171">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7ead9-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ead9-172">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="7ead9-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7ead9-173">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="7ead9-173">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="7ead9-174">**Lettura non valida** (4)</span><span class="sxs-lookup"><span data-stu-id="7ead9-174">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="7ead9-175">**Errore di parità** (5)</span><span class="sxs-lookup"><span data-stu-id="7ead9-175">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="7ead9-176">**Errore a bit singolo** (6)</span><span class="sxs-lookup"><span data-stu-id="7ead9-176">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="7ead9-177">**Errore a doppio bit** (7)</span><span class="sxs-lookup"><span data-stu-id="7ead9-177">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="7ead9-178">**Errore a più bit** (8)</span><span class="sxs-lookup"><span data-stu-id="7ead9-178">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="7ead9-179">**Errore di roditura** (9)</span><span class="sxs-lookup"><span data-stu-id="7ead9-179">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="7ead9-180">**Errore di checksum** (10)</span><span class="sxs-lookup"><span data-stu-id="7ead9-180">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="7ead9-181">**Errore CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="7ead9-181">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="7ead9-182">Non **definito** (12)</span><span class="sxs-lookup"><span data-stu-id="7ead9-182">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="7ead9-183">Non **definito** (13)</span><span class="sxs-lookup"><span data-stu-id="7ead9-183">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="7ead9-184">Non **definito** (14)</span><span class="sxs-lookup"><span data-stu-id="7ead9-184">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ead9-185">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="7ead9-185">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7ead9-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-188">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-188">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-189">Indica se gli algoritmi di parità, gli algoritmi CRC, ECC o altri meccanismi vengono utilizzati dall'oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="7ead9-189">Indicates whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used by the memory object.</span></span> <span data-ttu-id="7ead9-190">È anche possibile specificare i dettagli sull'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="7ead9-190">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-191">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="7ead9-191">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-192">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ead9-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-194">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorResolution"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,21 "," MIF. DMTF \| matrice di memoria fisica \| 001,15 "), **punito** (" byte ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-194">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.21", "MIF.DMTF\|Physical Memory Array\|001.15"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-195">Intervallo, in byte, in cui è possibile risolvere l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="7ead9-195">The range, in bytes, in which the last error can be resolved.</span></span> <span data-ttu-id="7ead9-196">Ad esempio, se gli indirizzi di errore vengono risolti in bit 11, ad esempio in base a una pagina tipica; gli errori possono quindi essere risolti in limiti di 4K e questa proprietà è impostata su "4000".</span><span class="sxs-lookup"><span data-stu-id="7ead9-196">For example, if error addresses are resolved to bit 11, such as on a typical page basis; then the errors can be resolved to 4K boundaries, and this property is set to "4000".</span></span> <span data-ttu-id="7ead9-197">Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7ead9-197">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-198">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="7ead9-198">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-199">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7ead9-199">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-201">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTime")</span><span class="sxs-lookup"><span data-stu-id="7ead9-201">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTime")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-202">Ora in cui si è verificato l'ultimo errore di memoria.</span><span class="sxs-lookup"><span data-stu-id="7ead9-202">The time when the last memory error occurred.</span></span> <span data-ttu-id="7ead9-203">Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7ead9-203">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-204">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="7ead9-204">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-205">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7ead9-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-207">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTransferSize"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| array di memoria fisica \| 001,11 "), **punito** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-207">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTransferSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.11"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-208">Dimensioni del trasferimento dati, in bit, che hanno causato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="7ead9-208">The size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="7ead9-209">"0" indica che non è presente alcun errore.</span><span class="sxs-lookup"><span data-stu-id="7ead9-209">"0" indicates no error.</span></span> <span data-ttu-id="7ead9-210">Se la proprietà **errorInfo** contiene "3" (OK), questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7ead9-210">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-211">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7ead9-211">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-212">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7ead9-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-214">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="7ead9-214">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-215">Descrizione del tipo di errore, quando la proprietà **ErrorType** è impostata su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="7ead9-215">A description of the error type, when the **ErrorType** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-216">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="7ead9-216">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-217">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ead9-217">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-219">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,3 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,4 "), **punito** (" byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="7ead9-219">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-220">Indirizzo iniziale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per l'oggetto memoria.</span><span class="sxs-lookup"><span data-stu-id="7ead9-220">The starting address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="7ead9-221">L'indirizzo iniziale è specificato in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="7ead9-221">The starting address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-222">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="7ead9-222">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-223">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ead9-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-225">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.SystemLevelAddress")</span><span class="sxs-lookup"><span data-stu-id="7ead9-225">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.SystemLevelAddress")</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-226">**true** se le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema, **false** se è un indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="7ead9-226">**true** if the address information in the **ErrorAddress** property is a system-level address, **false** if it is a physical address.</span></span>

</dd> <dt>

<span data-ttu-id="7ead9-227">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="7ead9-227">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead9-228">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ead9-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ead9-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ead9-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ead9-230">**true** se la memoria è volatile; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7ead9-230">**true** if the memory is volatile; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ead9-231">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ead9-231">Requirements</span></span>



| <span data-ttu-id="7ead9-232">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ead9-232">Requirement</span></span> | <span data-ttu-id="7ead9-233">Valore</span><span class="sxs-lookup"><span data-stu-id="7ead9-233">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ead9-234">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ead9-234">Minimum supported client</span></span><br/> | <span data-ttu-id="7ead9-235">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ead9-235">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7ead9-236">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ead9-236">Minimum supported server</span></span><br/> | <span data-ttu-id="7ead9-237">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ead9-237">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7ead9-238">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7ead9-238">Namespace</span></span><br/>                | <span data-ttu-id="7ead9-239">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7ead9-239">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7ead9-240">MOF</span><span class="sxs-lookup"><span data-stu-id="7ead9-240">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ead9-241"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ead9-241"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ead9-242">DLL</span><span class="sxs-lookup"><span data-stu-id="7ead9-242">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ead9-243"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ead9-243"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7ead9-244">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ead9-244">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ead9-245">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7ead9-245">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

