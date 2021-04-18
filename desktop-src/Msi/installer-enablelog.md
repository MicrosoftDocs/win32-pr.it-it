---
description: Il metodo EnableLog dell'oggetto Installer consente la registrazione del tipo di messaggio selezionato per tutte le sessioni di installazione successive nello spazio di processo corrente.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Installer. EnableLog, metodo
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
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324645"
---
# <a name="installerenablelog-method"></a>Installer. EnableLog, metodo

Il metodo **EnableLog** dell'oggetto [**Installer**](installer-object.md) consente la registrazione del tipo di messaggio selezionato per tutte le sessioni di installazione successive nello spazio di processo corrente.

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

Stringa obbligatoria che contiene le lettere che rappresentano i tipi di messaggio da registrare. La stringa può essere una combinazione dei valori seguenti.



| Valore | Descrizione                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | Messaggi di sola informazione.                                                                             |
| w     | Messaggi di avviso non irreversibili.                                                                            |
| h     | Messaggi di errore che potrebbero essere errori irreversibili.                                                               |
| f     | Elenco di file in uso che devono essere sostituiti.                                                         |
| a     | Inizio della notifica dell'azione.                                                                          |
| r     | Record di dati azione che contiene contenuto specifico per l'azione.                                              |
| u     | Messaggi di richiesta dell'utente.                                                                                 |
| c     | Parametri di inizializzazione dell'interfaccia utente.                                                                          |
| m     | Messaggio di memoria insufficiente.                                                                                 |
| v     | Invia grandi quantità di informazioni al file di log non in genere utile agli utenti. Può essere utilizzato per il supporto. |
| p     | Dump della tabella delle proprietà; "Property = Value" alla chiusura del motore                                          |
| \+    | Accoda a un file di log esistente.                                                                           |
| !     | Scaricare ogni riga nel file di log.                                                                       |
| x     | Informazioni di debug aggiuntive. Questa opzione è disponibile solo con Windows Server 2003.                      |
| o     | Messaggi di spazio fuori disco.                                                                            |



 

</dd> <dt>

*logFile* 
</dt> <dd>

Stringa obbligatoria contenente il percorso del file di log da creare. Usare una stringa vuota ("") per disattivare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il percorso del file di log deve esistere già quando si usa questo metodo. Il programma di installazione non crea la struttura di directory per il file di log.

Le opzioni di registrazione impostate utilizzando **EnableLog** sostituiscono le impostazioni dei criteri di registrazione Windows Installer esistenti.

Per impostazione predefinita, la registrazione sovrascrive un file di log esistente. Per aggiungere un file di log esistente, è necessario utilizzare la lettera "+" nella modalità di registrazione.

L'opzione '!' non è consigliata perché può rallentare notevolmente l'installazione. Questa opzione può essere utile quando si esegue il debug di un'installazione.

Lo script di esempio seguente attiva la registrazione dettagliata per un'installazione. Al termine dell'installazione, il file di log generato sarà in c: \\ temp \\ Install. log.


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Registrazione Windows Installer](windows-installer-logging.md)
</dt> </dl>

 

 




