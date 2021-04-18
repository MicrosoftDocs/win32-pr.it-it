---
description: Il metodo Import dell'oggetto di database importa una tabella di database da un file di archivio di testo, eliminando tutte le tabelle esistenti.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Metodo database. Import
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
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327663"
---
# <a name="databaseimport-method"></a>Metodo database. Import

Il metodo **Import** dell'oggetto di [**database**](database-object.md) importa una tabella di database da un file di [Archivio di testo](text-archive-files.md), eliminando tutte le tabelle esistenti.

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

Nome obbligatorio del file da importare. Questa operazione non include la cartella, che deve essere impostata nell'oggetto Path. Il nome della tabella viene specificato all'interno del file.

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
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Database**](database-object.md)
</dt> <dt>

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




