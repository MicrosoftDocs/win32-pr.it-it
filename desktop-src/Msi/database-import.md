---
description: Il metodo Import dell'oggetto Database importa una tabella di database da un file di archivio di testo, eliminando qualsiasi tabella esistente.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Metodo Database.Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31bd306475460b03e9b4b5137cbd8fe214128dbec0dac516d2d9557de137a82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075031"
---
# <a name="databaseimport-method"></a>Metodo Database.Import

Il **metodo Import** dell'oggetto [**Database**](database-object.md) importa una tabella di database da un file di archivio [di testo,](text-archive-files.md)eliminando qualsiasi tabella esistente.

## <a name="syntax"></a>Sintassi


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*path* 
</dt> <dd>

Cartella obbligatoria in cui è presente il file di testo.

</dd> <dt>

*file* 
</dt> <dd>

Nome obbligatorio del file da importare. Non include la cartella , perché deve essere impostata nell'oggetto path. Il nome della tabella viene specificato all'interno del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Database**](database-object.md)
</dt> <dt>

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




