---
description: Il metodo Export dell'oggetto di database copia la struttura e i dati da una tabella specificata in un file di archivio di testo.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Metodo database. Export
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
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326544"
---
# <a name="databaseexport-method"></a>Metodo database. Export

Il metodo **Export** dell'oggetto di [**database**](database-object.md) copia la struttura e i dati da una tabella specificata in un file di [Archivio di testo](text-archive-files.md).

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

Nome obbligatorio della tabella di database. Distinzione tra maiuscole e minuscole se si usa il database di installazione.

</dd> <dt>

*path* 
</dt> <dd>

Stringa obbligatoria che rappresenta il percorso della cartella in cui è inserito il file di testo.

</dd> <dt>

*file* 
</dt> <dd>

Nome obbligatorio del file da creare. Questa operazione non include la cartella, che deve essere impostata nell'oggetto Path.

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



 

 




