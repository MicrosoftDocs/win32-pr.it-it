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
# <a name="sense_data-structure"></a>\_Struttura dei dati di rilevamento

Utilizzato per segnalare informazioni sullo stato o sugli errori in risposta a un comando di **richiesta** SCSI.

## <a name="syntax"></a>Sintassi


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



## <a name="members"></a>Members

<dl> <dt>

**ErrorCode**
</dt> <dd>

Tipo di report.



| Valore                                                                           | Significato                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0x70</dt> </dl> | Errori correnti.<br/>  |
| <dl> <dt>0x71</dt> </dl> | Errori posticipati.<br/> |



 

</dd> <dt>

**Valido**
</dt> <dd>

1 se il campo **informazioni** è definito in uno standard; in caso contrario, il campo **informazioni** è specifico del fornitore e non è definito da uno standard.

</dd> <dt>

**SegmentNumber**
</dt> <dd>

Obsoleta.

</dd> <dt>

**SenseKey**
</dt> <dd>

Indica la categoria di errore.

<dl> <dt>

<span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Nessun senso** (0x0)
</dt> <dt>

<span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Errore recuperato** (0x1)
</dt> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (0x2)
</dt> <dt>

<span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Errore medio** (0x3)
</dt> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Errore hardware** (0x4)
</dt> <dt>

<span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Richiesta non valida** (0x5)
</dt> <dt>

<span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Attenzione unità** (0x6)
</dt> <dt>

<span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Protezione dei dati** (0x7)
</dt> <dt>

<span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Errore del firmware** (0x9)
</dt> <dt>

<span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Comando interrotto** (0xB)
</dt> <dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Uguale** (0xC)
</dt> <dt>

<span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Overflow del volume** (0xD)
</dt> <dt>

<span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Confronto non confrontato** (0xe)
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**IncorrectLength**
</dt> <dd>

1 se la lunghezza del blocco logico richiesta non corrisponde alla lunghezza del blocco logico dei dati sul supporto.

</dd> <dt>

**EndOfMedia**
</dt> <dd>

1 se un dispositivo con accesso sequenziale ha raggiunto la fine del supporto o se una stampante è fuori carta.

</dd> <dt>

**Contrassegno**
</dt> <dd>

1 se il comando corrente ha raggiunto un oggetto filemark o un contrassegno. Valido solo per i dispositivi con accesso sequenziale.

</dd> <dt>

**Informazioni**
</dt> <dd>

Dati specifici del tipo di dispositivo o del comando.

</dd> <dt>

**AdditionalSenseLength**
</dt> <dd>

Lunghezza in byte del resto della struttura. Lunghezza totale meno 7.

</dd> <dt>

**CommandSpecificInformation**
</dt> <dd>

Dati specifici del comando. I valori sono definiti nello standard del comando appropriato.

</dd> <dt>

**AdditionalSenseCode**
</dt> <dd>

Codice specifico del dispositivo che descrive l'errore riportato nel campo **SenseKey** .

</dd> <dt>

**AdditionalSenseCodeQualifier**
</dt> <dd>

Può contenere dettagli aggiuntivi sul campo **AdditionalSenseCode** .

</dd> <dt>

**FieldReplaceableUnitCode**
</dt> <dd>

Informazioni specifiche dei venditori sul componente associato a questi dati di rilevamento.

</dd> <dt>

**SenseKeySpecific**
</dt> <dd>

Il contenuto e il formato delle informazioni specifiche della chiave di senso sono determinati dal valore del campo **SenseKey** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sul formato dei dati Sense, vedere [comando SCSI Request Sense](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>SCSI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Pass-through di destinazione iSCSI](/powershell/module/iscsi)
</dt> <dt>

[\_pass- \_ through \_ diretto SCSI](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




