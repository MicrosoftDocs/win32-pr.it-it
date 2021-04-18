---
description: Il metodo sestream dell'oggetto record copia il contenuto del file specificato nel campo record designato come dati di flusso. Non è possibile inserire i dati del flusso in campi temporanei.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Metodo record. sestream
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
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330920"
---
# <a name="recordsetstream-method"></a>Metodo record. sestream

Il metodo **sestream** dell'oggetto [**record**](record-object.md) copia il contenuto del file specificato nel campo record designato come dati di flusso. Non è possibile inserire i dati del flusso in campi temporanei.

## <a name="syntax"></a>Sintassi


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*campo* 
</dt> <dd>

Numero di campo obbligatorio del valore all'interno del record, basato su 1.

</dd> <dt>

*filePath* 
</dt> <dd>

Percorso del file da copiare. Non viene eseguita alcuna conversione di alcun tipo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




