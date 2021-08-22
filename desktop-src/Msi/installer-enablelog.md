---
description: Il metodo EnableLog dell'oggetto Installer abilita la registrazione del tipo di messaggio selezionato per tutte le sessioni di installazione successive nello spazio del processo corrente.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Metodo Installer.EnableLog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 48481a701b7e78de372f5579dab5c9d5976a68063958b0812d6ae1ddc08b109a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631697"
---
# <a name="installerenablelog-method"></a>Metodo Installer.EnableLog

Il **metodo EnableLog** dell'oggetto [**Installer**](installer-object.md) abilita la registrazione del tipo di messaggio selezionato per tutte le sessioni di installazione successive nello spazio del processo corrente.

## <a name="syntax"></a>Sintassi


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*logMode* 
</dt> <dd>

Stringa obbligatoria che contiene lettere che rappresentano i tipi di messaggio da registrare. La stringa può essere una combinazione dei valori seguenti.



| Valore | Descrizione                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | Messaggi di sola informazione.                                                                             |
| w     | Messaggi di avviso non irreversibili.                                                                            |
| h     | Messaggi di errore che possono essere errori irreversibili.                                                               |
| f     | Elenco di file in uso che devono essere sostituiti.                                                         |
| a     | Inizio della notifica dell'azione.                                                                          |
| r     | Record di dati dell'azione contenente il contenuto specifico dell'azione.                                              |
| u     | Messaggi di richiesta dell'utente.                                                                                 |
| c     | Parametri di inizializzazione dell'interfaccia utente.                                                                          |
| m     | Messaggio di memoria insufficiente.                                                                                 |
| v     | Invia grandi quantità di informazioni al file di log non in genere utili agli utenti. Può essere usato per il supporto. |
| p     | Tabella delle proprietà dump; "property = value" alla terminazione del motore                                          |
| \+    | Aggiungere al file di log esistente.                                                                           |
| !     | Scaricare ogni riga nel file di log.                                                                       |
| x     | Informazioni di debug aggiuntive. Questa opzione è disponibile solo con Windows Server 2003.                      |
| o     | Messaggi di spazio su disco insufficiente.                                                                            |



 

</dd> <dt>

*Logfile* 
</dt> <dd>

Stringa obbligatoria contenente il percorso del file di log da creare. Usare una stringa vuota ("") per disattivare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il percorso del file di log deve esistere già quando si usa questo metodo. Il programma di installazione non crea la struttura di directory per il file di log.

Le opzioni di registrazione impostate tramite **EnableLog** sostituiscono le impostazioni dei criteri Windows di registrazione del programma di installazione.

Per impostazione predefinita, la registrazione sovrascrive un file di log esistente. È necessario usare la lettera "+" in modalità di registrazione per aggiungere a un file di log esistente.

L'opzione '!' non è consigliata perché può rallentare notevolmente l'installazione. Questa opzione può essere utile quando si esegue il debug di un'installazione.

Lo script di esempio seguente attiva la registrazione dettagliata per un'installazione. Al termine dell'installazione, il file di log generato sarà in \\ c:temp \\ install.log.


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Registrazione del programma di installazione](windows-installer-logging.md)
</dt> </dl>

 

 




