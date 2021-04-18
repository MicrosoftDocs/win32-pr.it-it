---
description: Il metodo OpenDatabase dell'oggetto Installer apre un database esistente o ne crea uno nuovo, restituendo un oggetto di database. Se non è possibile creare e aprire correttamente l'oggetto di database, viene generato un errore.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer. OpenDatabase, metodo
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
ms.openlocfilehash: 13256f0bbe2d5adad61c46ea091e8207f1a9351b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324610"
---
# <a name="installeropendatabase-method"></a>Installer. OpenDatabase, metodo

Il metodo **OpenDatabase** dell'oggetto [**Installer**](installer-object.md) apre un database esistente o ne crea uno nuovo, restituendo un oggetto di [**database**](database-object.md) . Se non è possibile creare e aprire correttamente l'oggetto di **database** , viene generato un errore.

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

Stringa obbligatoria che contiene il nome del percorso del database. Se viene fornita una stringa vuota, viene creato un database temporaneo che non viene reso permanente.

</dd> <dt>

*openMode* 
</dt> <dd>

Un parametro dell'elenco seguente o una stringa che contiene il nome del percorso del nuovo file di database di output in cui scrivere al momento del commit.



| Parametro                                                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt> </dl>                 | Apre un database di sola lettura, senza modifiche permanenti.<br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt> </dl>                 | Apre un database di lettura/scrittura in modalità transazione.<br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt> </dl>                         | Apre una lettura/scrittura diretta del database senza transazione.<br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt> </dl>                         | Consente di creare un nuovo database, in modalità Transact-lettura/scrittura.<br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt> </dl> | Crea un nuovo database, modalità diretta di lettura/scrittura.<br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt> </dl>         | Apre un database per visualizzare i file di script di annuncio, ad esempio i file generati dal metodo [**CreateAdvertiseScript**](installer-createadvertisescript.md) .<br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt> </dl>            | Aggiunge questo flag per indicare un file di correzione.<br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando un database viene aperto come output di un altro database, il flusso di informazioni di riepilogo del database di output è effettivamente un mirror di sola lettura del database originale e pertanto non può essere modificato. Inoltre, non viene reso permanente con il database. Per creare o modificare le informazioni di riepilogo per il database di output, è necessario chiuderlo e riaprirlo.

Per creare e salvare le modifiche apportate a un database, aprire innanzitutto il database nella modalità transazione (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate o msiOpenDatabaseModeCreateDirect) o Direct (msiOpenDatabaseModeDirect). Dopo avere apportato le modifiche, chiamare sempre il metodo [**commit**](database-commit.md) prima di chiudere l'handle di database. Il metodo **commit** Scarica tutti i buffer.

Chiamare sempre il metodo [**commit**](database-commit.md) su un database aperto in modalità diretta (MsiOpenDatabaseModeDirect o msiOpenDatabaseModeCreateDirect) prima di chiudere il database. In caso contrario, è possibile che il database sia danneggiato.

Poiché il metodo **OpenDatabase** avvia l'accesso al database, non può essere utilizzato con un'installazione in esecuzione.

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




