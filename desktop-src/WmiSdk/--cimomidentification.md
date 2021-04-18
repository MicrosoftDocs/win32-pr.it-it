---
description: Descrive l'installazione locale di WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: Classe __CIMOMIdentification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314096"
---
# <a name="__cimomidentification-class"></a>\_\_Classe CIMOMIdentification

La classe di sistema **\_ \_ CIMOMIdentification** descrive l'installazione locale di WMI. Si tratta di una classe singleton; esiste una sola istanza. La classe **\_ \_ CIMOMIdentification** è disponibile solo negli spazi dei nomi **\\ predefiniti** **radice** e radice. Gli utenti eseguono una query per l'istanza di per ottenere informazioni sull'installazione di WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a>Members

La classe **\_ \_ CIMOMIdentification** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ CIMOMIdentification** dispone di queste proprietà.

<dl> <dt>

**SetupDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'installazione. Questa proprietà è vuota dopo l'installazione del sistema operativo per la prima volta.

Se il repository WMI è stato eliminato e quindi creato nuovamente, questa proprietà contiene la data e l'ora di creazione del repository.

</dd> <dt>

**VersionCurrentlyRunning**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la versione dell'immagine effettiva contenente il servizio WMI che ha creato il repository di Common Information Model (CIM). Poiché il formato del repository può variare tra le versioni di WMI, questa proprietà consente aggiornamenti WMI futuri per determinare se è necessario aggiornare il database. Il formato è:

"1.00.183.0000"

Se la prima cifra è la versione principale, le due cifre successive sono le versioni secondarie e le tre cifre successive corrispondono al numero di Build. Le cifre rimanenti non vengono utilizzate.

</dd> <dt>

**VersionUsedToCreateDB**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la versione dell'immagine effettiva contenente il servizio WMI che ha creato il repository CIM. Poiché il formato del repository può variare tra le versioni di WMI, questa proprietà consente aggiornamenti WMI futuri per determinare se è necessario aggiornare il database. Il formato è:

"1.00.183.0000"

Se la prima cifra è la versione principale, le due cifre successive sono le versioni secondarie e le tre cifre successive corrispondono al numero di Build. Le cifre rimanenti non vengono utilizzate.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Directory di installazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ CIMOMIdentification** deriva da [**\_ \_ SystemClass**](--systemclass.md), che non dispone di proprietà.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript riportato di seguito viene descritto come visualizzare le informazioni di identificazione del modello a oggetti CIM ed è stato ricavato dalla directory di esempio in \\ \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ sysmgmt di \\ \\ script WMI.


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



Nell'esempio di codice Perl seguente viene descritto come visualizzare le informazioni di identificazione del modello a oggetti CIM ed è stato ricavato dalla directory di esempio in \\ \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ sysmgmt di \\ \\ script WMI.


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Radice<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

