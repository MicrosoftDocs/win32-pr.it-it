---
description: Utilizzato per segnalare informazioni sullo stato o sugli errori in risposta a un comando di richiesta SCSI.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: Struttura SENSE_DATA (SCSI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: b5eacf9bee8c2cebf93b27c97a88c691852a3841
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321097"
---
# <a name="sense_data-structure"></a><span data-ttu-id="67c69-103">\_Struttura dei dati di rilevamento</span><span class="sxs-lookup"><span data-stu-id="67c69-103">SENSE\_DATA structure</span></span>

<span data-ttu-id="67c69-104">Utilizzato per segnalare informazioni sullo stato o sugli errori in risposta a un comando di **richiesta** SCSI.</span><span class="sxs-lookup"><span data-stu-id="67c69-104">Used to report status or error information in response to a SCSI **Request Sense** command.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c69-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67c69-105">Syntax</span></span>


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a><span data-ttu-id="67c69-106">Members</span><span class="sxs-lookup"><span data-stu-id="67c69-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="67c69-107">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="67c69-107">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-108">Tipo di report.</span><span class="sxs-lookup"><span data-stu-id="67c69-108">The report type.</span></span>



| <span data-ttu-id="67c69-109">Valore</span><span class="sxs-lookup"><span data-stu-id="67c69-109">Value</span></span>                                                                           | <span data-ttu-id="67c69-110">Significato</span><span class="sxs-lookup"><span data-stu-id="67c69-110">Meaning</span></span>                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="67c69-111"><dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="67c69-111"><dt>0x70</dt></span></span> </dl> | <span data-ttu-id="67c69-112">Errori correnti.</span><span class="sxs-lookup"><span data-stu-id="67c69-112">Current errors.</span></span><br/>  |
| <dl> <span data-ttu-id="67c69-113"><dt>0x71</dt></span><span class="sxs-lookup"><span data-stu-id="67c69-113"><dt>0x71</dt></span></span> </dl> | <span data-ttu-id="67c69-114">Errori posticipati.</span><span class="sxs-lookup"><span data-stu-id="67c69-114">Deferred errors.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="67c69-115">**Valido**</span><span class="sxs-lookup"><span data-stu-id="67c69-115">**Valid**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-116">1 se il campo **informazioni** è definito in uno standard; in caso contrario, il campo **informazioni** è specifico del fornitore e non è definito da uno standard.</span><span class="sxs-lookup"><span data-stu-id="67c69-116">1 if the **Information** field is defined in a standard; otherwise the **Information** field is vendor-specific and not defined by a standard.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-117">**SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="67c69-117">**SegmentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-118">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="67c69-118">Obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-119">**SenseKey**</span><span class="sxs-lookup"><span data-stu-id="67c69-119">**SenseKey**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-120">Indica la categoria di errore.</span><span class="sxs-lookup"><span data-stu-id="67c69-120">Indicates the category of error.</span></span>

<dl> <dt>

<span data-ttu-id="67c69-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Nessun senso** (0x0)</span><span class="sxs-lookup"><span data-stu-id="67c69-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No Sense** (0x0)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Errore recuperato** (0x1)</span><span class="sxs-lookup"><span data-stu-id="67c69-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Recovered Error** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (0x2)</span><span class="sxs-lookup"><span data-stu-id="67c69-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Errore medio** (0x3)</span><span class="sxs-lookup"><span data-stu-id="67c69-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Medium Error** (0x3)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Errore hardware** (0x4)</span><span class="sxs-lookup"><span data-stu-id="67c69-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Richiesta non valida** (0x5)</span><span class="sxs-lookup"><span data-stu-id="67c69-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Illegal Request** (0x5)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Attenzione unità** (0x6)</span><span class="sxs-lookup"><span data-stu-id="67c69-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Unit Attention** (0x6)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Protezione dei dati** (0x7)</span><span class="sxs-lookup"><span data-stu-id="67c69-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Data Protect** (0x7)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Errore del firmware** (0x9)</span><span class="sxs-lookup"><span data-stu-id="67c69-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmware Error** (0x9)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Comando interrotto** (0xB)</span><span class="sxs-lookup"><span data-stu-id="67c69-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Aborted Command** (0xB)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Uguale** (0xC)</span><span class="sxs-lookup"><span data-stu-id="67c69-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Equal** (0xC)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Overflow del volume** (0xD)</span><span class="sxs-lookup"><span data-stu-id="67c69-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volume Overflow** (0xD)</span></span>
</dt> <dt>

<span data-ttu-id="67c69-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Confronto non confrontato** (0xe)</span><span class="sxs-lookup"><span data-stu-id="67c69-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Miscompare** (0xE)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="67c69-134">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="67c69-134">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-135">Riservato.</span><span class="sxs-lookup"><span data-stu-id="67c69-135">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-136">**IncorrectLength**</span><span class="sxs-lookup"><span data-stu-id="67c69-136">**IncorrectLength**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-137">1 se la lunghezza del blocco logico richiesta non corrisponde alla lunghezza del blocco logico dei dati sul supporto.</span><span class="sxs-lookup"><span data-stu-id="67c69-137">1 if the requested logical block length does not match the logical block length of the data on the media.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-138">**EndOfMedia**</span><span class="sxs-lookup"><span data-stu-id="67c69-138">**EndOfMedia**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-139">1 se un dispositivo con accesso sequenziale ha raggiunto la fine del supporto o se una stampante è fuori carta.</span><span class="sxs-lookup"><span data-stu-id="67c69-139">1 if a sequential-access device has reached end-of-media, or a printer is out of paper.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-140">**Contrassegno**</span><span class="sxs-lookup"><span data-stu-id="67c69-140">**FileMark**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-141">1 se il comando corrente ha raggiunto un oggetto filemark o un contrassegno.</span><span class="sxs-lookup"><span data-stu-id="67c69-141">1 if the current command has reached a filemark or setmark.</span></span> <span data-ttu-id="67c69-142">Valido solo per i dispositivi con accesso sequenziale.</span><span class="sxs-lookup"><span data-stu-id="67c69-142">Only valid for sequential-access devices.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-143">**Informazioni**</span><span class="sxs-lookup"><span data-stu-id="67c69-143">**Information**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-144">Dati specifici del tipo di dispositivo o del comando.</span><span class="sxs-lookup"><span data-stu-id="67c69-144">Device-type or command specific data.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-145">**AdditionalSenseLength**</span><span class="sxs-lookup"><span data-stu-id="67c69-145">**AdditionalSenseLength**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-146">Lunghezza in byte del resto della struttura.</span><span class="sxs-lookup"><span data-stu-id="67c69-146">The length in bytes of the remainder of the structure.</span></span> <span data-ttu-id="67c69-147">Lunghezza totale meno 7.</span><span class="sxs-lookup"><span data-stu-id="67c69-147">The total length minus 7.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-148">**CommandSpecificInformation**</span><span class="sxs-lookup"><span data-stu-id="67c69-148">**CommandSpecificInformation**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-149">Dati specifici del comando.</span><span class="sxs-lookup"><span data-stu-id="67c69-149">Command-specific data.</span></span> <span data-ttu-id="67c69-150">I valori sono definiti nello standard del comando appropriato.</span><span class="sxs-lookup"><span data-stu-id="67c69-150">Values are defined in the appropriate command standard.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-151">**AdditionalSenseCode**</span><span class="sxs-lookup"><span data-stu-id="67c69-151">**AdditionalSenseCode**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-152">Codice specifico del dispositivo che descrive l'errore riportato nel campo **SenseKey** .</span><span class="sxs-lookup"><span data-stu-id="67c69-152">Device specific code that describes the error reported in the **SenseKey** field.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-153">**AdditionalSenseCodeQualifier**</span><span class="sxs-lookup"><span data-stu-id="67c69-153">**AdditionalSenseCodeQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-154">Può contenere dettagli aggiuntivi sul campo **AdditionalSenseCode** .</span><span class="sxs-lookup"><span data-stu-id="67c69-154">Can contain additional detail about the **AdditionalSenseCode** field.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-155">**FieldReplaceableUnitCode**</span><span class="sxs-lookup"><span data-stu-id="67c69-155">**FieldReplaceableUnitCode**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-156">Informazioni specifiche dei venditori sul componente associato a questi dati di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="67c69-156">Vender-specific information about the component associated with this sense data.</span></span>

</dd> <dt>

<span data-ttu-id="67c69-157">**SenseKeySpecific**</span><span class="sxs-lookup"><span data-stu-id="67c69-157">**SenseKeySpecific**</span></span>
</dt> <dd>

<span data-ttu-id="67c69-158">Il contenuto e il formato delle informazioni specifiche della chiave di senso sono determinati dal valore del campo **SenseKey** .</span><span class="sxs-lookup"><span data-stu-id="67c69-158">The content and format of the sense key specific information is determined by the value of the **SenseKey** field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67c69-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="67c69-159">Remarks</span></span>

<span data-ttu-id="67c69-160">Per ulteriori informazioni sul formato dei dati Sense, vedere [comando SCSI Request Sense](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .</span><span class="sxs-lookup"><span data-stu-id="67c69-160">For more information about the sense data format, see [SCSI Request Sense Command](https://wikipedia.org/wiki/SCSI_command) (https://wikipedia.org/wiki/SCSI_command).</span></span>

## <a name="requirements"></a><span data-ttu-id="67c69-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67c69-161">Requirements</span></span>



| <span data-ttu-id="67c69-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c69-162">Requirement</span></span> | <span data-ttu-id="67c69-163">Valore</span><span class="sxs-lookup"><span data-stu-id="67c69-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="67c69-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67c69-164">Minimum supported client</span></span><br/> | <span data-ttu-id="67c69-165">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="67c69-165">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="67c69-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67c69-166">Minimum supported server</span></span><br/> | <span data-ttu-id="67c69-167">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="67c69-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="67c69-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67c69-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="67c69-169"><dt>SCSI. h</dt></span><span class="sxs-lookup"><span data-stu-id="67c69-169"><dt>Scsi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c69-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67c69-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c69-171">Pass-through di destinazione iSCSI</span><span class="sxs-lookup"><span data-stu-id="67c69-171">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="67c69-172">\_pass- \_ through \_ diretto SCSI</span><span class="sxs-lookup"><span data-stu-id="67c69-172">SCSI\_PASS\_THROUGH\_DIRECT</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




