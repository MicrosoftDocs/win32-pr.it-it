---
description: Il metodo Export dell'oggetto Database copia la struttura e i dati da una tabella specificata in un file di archivio di testo.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Metodo Database.Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: faa5e2459eb0fe4ba04fd548bc478c9a0e2c85267e1df8e3d318f4a3f6a082ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745611"
---
# <a name="databaseexport-method"></a>Metodo Database.Export

Il **metodo Export** dell'oggetto [**Database**](database-object.md) copia la struttura e i dati da una tabella specificata in un file di archivio [di testo](text-archive-files.md).

## <a name="syntax"></a>Sintassi


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tabella* 
</dt> <dd>

Nome obbligatorio della tabella di database. Fare distinzione tra maiuscole e minuscole se si usa il database del programma di installazione.

</dd> <dt>

*path* 
</dt> <dd>

Stringa obbligatoria che rappresenta il percorso della cartella in cui si trova il file di testo.

</dd> <dt>

*file* 
</dt> <dd>

Nome obbligatorio del file da creare. Non include la cartella , perché deve essere impostata nell'oggetto path.

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



 

 




