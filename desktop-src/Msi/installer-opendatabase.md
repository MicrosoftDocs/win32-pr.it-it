---
description: Il metodo OpenDatabase dell'oggetto Installer apre un database esistente o ne crea uno nuovo, che restituisce un oggetto Database. Se l'oggetto Database non può essere creato e aperto correttamente, viene generato un errore.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Metodo Installer.OpenDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 897e683fd56ce3e7496dd945ee068a9e6f0c0f77
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492270"
---
# <a name="installeropendatabase-method"></a>Metodo Installer.OpenDatabase

Il **metodo OpenDatabase** dell'oggetto [**Installer**](installer-object.md) apre un database esistente o ne crea uno nuovo, che restituisce un [**oggetto Database.**](database-object.md) Se l'oggetto **Database** non può essere creato e aperto correttamente, viene generato un errore.

## <a name="syntax"></a>Sintassi


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* 
</dt> <dd>

Stringa obbligatoria che contiene il nome del percorso del database. Se viene specificata una stringa vuota, viene creato un database temporaneo che non è persistente.

</dd> <dt>

*openMode* 
</dt> <dd>

Parametro dell'elenco seguente o stringa contenente il nome del percorso del nuovo file di database di output in cui scrivere al momento del commit.



| Parametro                                                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt> </dl>                 | Apre un database di sola lettura, senza modifiche persistenti.<br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt> </dl>                 | Apre un database in lettura/scrittura in modalità transazione.<br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt> </dl>                         | Apre un database di lettura/scrittura diretta senza transazione.<br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt> </dl>                         | Crea un nuovo database, lettura/scrittura in modalità transazione.<br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt> </dl> | Crea un nuovo database, lettura/scrittura in modalità diretta.<br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt> </dl>         | Apre un database per visualizzare i file script di annuncio, ad esempio i file generati dal [**metodo CreateAdvertiseScript.**](installer-createadvertisescript.md)<br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt> </dl>            | Aggiunge questo flag per indicare un file di patch.<br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**Database**](database-object.md) che rappresenta il database del programma di installazione esistente o nuovo aperto.

## <a name="remarks"></a>Commenti

Quando un database viene aperto come output di un altro database, il flusso di informazioni di riepilogo del database di output è in realtà un mirror di sola lettura del database originale e pertanto non può essere modificato. Inoltre, non viene salvato in modo permanente con il database. Per creare o modificare le informazioni di riepilogo per il database di output, è necessario chiuderlo e riaprirlo.

Per apportare e salvare le modifiche a un database, aprire prima il database in modalità transazione (msiOpenDatabaseModeTransact), creare (msiOpenDatabaseModeCreate o msiOpenDatabaseModeCreateDirect) o in modalità diretta (msiOpenDatabaseModeDirect). Dopo aver apportato le modifiche, chiamare sempre il [**metodo Commit**](database-commit.md) prima di chiudere l'handle del database. Il **metodo Commit** scarica tutti i buffer.

Chiamare sempre il [**metodo Commit**](database-commit.md) su un database aperto in modalità diretta (msiOpenDatabaseModeDirect o msiOpenDatabaseModeCreateDirect) prima di chiudere il database. In caso negativo, il database potrebbe essere danneggiato.

Poiché il **metodo OpenDatabase avvia** l'accesso al database, non può essere usato con un'installazione in esecuzione.

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5.0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




