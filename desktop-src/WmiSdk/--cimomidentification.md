---
description: Descrive l'installazione locale di WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: __CIMOMIdentification classe
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
ms.openlocfilehash: 50d81fb8cfc5580ad0868df307771c493c0919e1bf2ce4de4b67d48db034a0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321111"
---
# <a name="__cimomidentification-class"></a>\_\_Classe CIMOMIdentification

La **\_ \_ classe di sistema CIMOMIdentification** descrive l'installazione locale di WMI. Si tratta di una classe singleton. è presente una sola istanza. La **\_ \_ classe CIMOMIdentification** è disponibile solo negli spazi dei nomi **Root** e **Root \\ Default.** Gli utenti esere query per l'istanza di per ottenere informazioni sull'installazione di WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **\_ \_ classe CIMOMIdentification** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe CIMOMIdentification** ha queste proprietà.

<dl> <dt>

**SetupDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di installazione. Questa proprietà è vuota dopo la prima installazione del sistema operativo.

Se il repository WMI è stato eliminato e quindi creato di nuovo, questa proprietà contiene la data e l'ora di creazione del repository.

</dd> <dt>

**VersionCurrentlyRunning**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la versione dell'immagine effettiva contenente il servizio WMI che ha creato il repository Common Information Model (CIM). Poiché il formato del repository può cambiare tra le versioni di WMI, questa proprietà consente agli aggiornamenti WMI futuri di determinare se il database deve essere aggiornato. Il formato è:

"1.00.183.0000"

dove la prima cifra è la versione principale, le due cifre successive sono versioni secondarie e le tre cifre successive sono il numero di build. Le cifre rimanenti non vengono usate.

</dd> <dt>

**VersionUsedToCreateDB**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la versione dell'immagine effettiva contenente il servizio WMI che ha creato il repository CIM. Poiché il formato del repository può cambiare tra le versioni di WMI, questa proprietà consente agli aggiornamenti WMI futuri di determinare se il database deve essere aggiornato. Il formato è:

"1.00.183.0000"

dove la prima cifra è la versione principale, le due cifre successive sono versioni secondarie e le tre cifre successive sono il numero di build. Le cifre rimanenti non vengono usate.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Directory di installazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe CIMOMIdentification** è derivata da [**\_ \_ SystemClass**](--systemclass.md), che non dispone di proprietà.

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente descrive come visualizzare le informazioni di identificazione del modello a oggetti CIM ed è stato tratto dalla directory di esempio in \\ \\ Programmi Microsoft SDK Windows \\ \\ \\ v7.0 \\ Samples \\ sysmgmt \\ wmi scripting \\ .


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



L'esempio di codice Perl seguente descrive come visualizzare le informazioni di identificazione del modello a oggetti CIM ed è stato tratto dalla directory di esempio in Programmi \\ \\ Microsoft SDK Windows \\ \\ \\ v7.0 \\ Samples \\ sysmgmt \\ wmi scripting \\ .


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

 

