---
description: Il metodo ReadStream dell'oggetto record legge un numero specificato di byte da un campo record che contiene dati di flusso.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Metodo record. ReadStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328766"
---
# <a name="recordreadstream-method"></a>Metodo record. ReadStream

Il metodo **ReadStream** dell'oggetto [**record**](record-object.md) legge un numero specificato di byte da un campo record che contiene dati di flusso.

## <a name="syntax"></a>Sintassi


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*campo* 
</dt> <dd>

Il numero di campo obbligatorio del valore all'interno del record, basato su 1.

</dd> <dt>

*length* 
</dt> <dd>

Numero necessario di byte da leggere dal flusso.

</dd> <dt>

*format* 
</dt> <dd>

Interpretazione richiesta e restituzione dei byte di dati.



| Nome parametro                                                                                                                                                                                                                                                                  | Significato                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <dt>**msiReadStreamInteger**</dt> <dt>0</dt> </dl> | Come Long Integer, la lunghezza deve essere compresa tra 1 e 4.<br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <dt>**msiReadStreamBytes**</dt> <dt>1</dt> </dl>         | Dati come **BSTR**, ovvero un byte per carattere.<br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <dt>**msiReadStreamAnsi**</dt> <dt>2</dt> </dl>             | Byte ANSI convertiti in un **BSTR** Unicode.<br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <dt>**msiReadStreamDirect**</dt> <dt>3</dt> </dl>     | Coppie di byte restituite direttamente come **BSTR**.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una stringa che contiene il numero di byte richiesto letti da un campo di record.

## <a name="remarks"></a>Commenti

Il valore restituito di un campo inesistente è un valore vuoto. Se il flusso ha un minor numero di byte richiesti dal conteggio, la stringa restituita viene abbreviata in modo appropriato.

Per un esempio di questo metodo, vedere [copiare il file ANSI in un campo del database](copy-ansi-file-into-a-database-field.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




