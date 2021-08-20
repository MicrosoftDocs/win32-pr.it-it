---
description: Consente di segnalare informazioni sullo stato o sull'errore in risposta a un comando SCSI Request Sense.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: SENSE_DATA struttura (Scsi.h)
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
ms.openlocfilehash: 2f6b3bd9fd4353e396bc7fe4ff7273e598704d1348062fec1c2f64aed9380686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075954"
---
# <a name="sense_data-structure"></a>Struttura SENSE \_ DATA

Consente di segnalare informazioni sullo stato o sull'errore in risposta a un comando SCSI **Request Sense.**

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
| <dl> <dt>0x71</dt> </dl> | Errori posticimanti.<br/> |



 

</dd> <dt>

**Valido**
</dt> <dd>

1 se il **campo** Informazioni è definito in uno standard; In caso **contrario,** il campo Informazioni è specifico del fornitore e non è definito da uno standard.

</dd> <dt>

**SegmentNumber**
</dt> <dd>

Obsoleta.

</dd> <dt>

**SenseKey**
</dt> <dd>

Indica la categoria di errore.

<dl> <dt>

<span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No Sense** (0x0)
</dt> <dt>

<span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Errore recuperato** (0x1)
</dt> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (0x2)
</dt> <dt>

<span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Errore medio** (0x3)
</dt> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Errore hardware** (0x4)
</dt> <dt>

<span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Richiesta non** valida (0x5)
</dt> <dt>

<span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Attenzione unità** (0x6)
</dt> <dt>

<span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Protezione dei** dati (0x7)
</dt> <dt>

<span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Errore firmware** (0x9)
</dt> <dt>

<span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Comando interrotto** (0xB)
</dt> <dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Uguale** (0xC)
</dt> <dt>

<span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volume Overflow** (0xD)
</dt> <dt>

<span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Non conforme** (0xE)
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**IncorrectLength**
</dt> <dd>

1 se la lunghezza del blocco logico richiesta non corrisponde alla lunghezza del blocco logico dei dati nel supporto.

</dd> <dt>

**EndOfMedia**
</dt> <dd>

1 se un dispositivo ad accesso sequenziale ha raggiunto la fine del supporto o se la carta di una stampante è scaduta.

</dd> <dt>

**FileMark**
</dt> <dd>

1 se il comando corrente ha raggiunto un contrassegno file o setmark. Valido solo per i dispositivi ad accesso sequenziale.

</dd> <dt>

**Informazioni**
</dt> <dd>

Dati specifici del tipo di dispositivo o del comando.

</dd> <dt>

**AdditionalSenseLength**
</dt> <dd>

Lunghezza in byte del resto della struttura . Lunghezza totale meno 7.

</dd> <dt>

**CommandSpecificInformation**
</dt> <dd>

Dati specifici del comando. I valori sono definiti nello standard di comando appropriato.

</dd> <dt>

**AdditionalSenseCode**
</dt> <dd>

Codice specifico del dispositivo che descrive l'errore segnalato nel **campo SenseKey.**

</dd> <dt>

**AdditionalSenseCodeQualifier**
</dt> <dd>

Può contenere dettagli aggiuntivi sul **campo AdditionalSenseCode.**

</dd> <dt>

**FieldReplaceableUnitCode**
</dt> <dd>

Informazioni specifiche di Vender sul componente associato a questi dati di senso.

</dd> <dt>

**SenseKeySpecific**
</dt> <dd>

Il contenuto e il formato delle informazioni specifiche della chiave di senso sono determinati dal valore del **campo SenseKey.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Per altre informazioni sul formato dei dati di sense, vedere [SCSI Request Sense Command](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Scsi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Pass-through di destinazione iSCSI](/powershell/module/iscsi)
</dt> <dt>

[SCSI \_ \_ PASS-THROUGH \_ DIRECT](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




