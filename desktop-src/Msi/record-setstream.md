---
description: Il metodo SetStream dell'oggetto Record copia il contenuto del file specificato nel campo di record designato come dati di flusso. I dati del flusso non possono essere inseriti in campi temporanei.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Metodo Record.SetStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de443f2d6802fb74e4b0f05b90ca8d3b3f97e328991fde50ec05ff37c203943c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626971"
---
# <a name="recordsetstream-method"></a>Metodo Record.SetStream

Il **metodo SetStream** dell'oggetto [**Record**](record-object.md) copia il contenuto del file specificato nel campo di record designato come dati di flusso. I dati del flusso non possono essere inseriti in campi temporanei.

## <a name="syntax"></a>Sintassi


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Campo* 
</dt> <dd>

Numero di campo obbligatorio del valore all'interno del record, in base 1.

</dd> <dt>

*Filepath* 
</dt> <dd>

Percorso del file da copiare. Non viene eseguita alcuna conversione di alcun tipo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




