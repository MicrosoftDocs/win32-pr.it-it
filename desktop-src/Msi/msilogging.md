---
description: La proprietà MsiLogging imposta la modalità di registrazione predefinita per il pacchetto Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: MsiLogging - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e166a52e970cdb3e0be5ffae6611a8ea9a299232d55f36a45ba470b3717cafae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042781"
---
# <a name="msilogging-property"></a>MsiLogging - proprietà

La **proprietà MsiLogging** imposta la modalità di registrazione predefinita per il pacchetto Windows Installer. Se questa proprietà facoltativa è presente nella tabella Property , il programma [di](property-table.md)installazione genera un file di log denominato \* MSI. Registro. Il percorso completo del file di log viene specificato dal valore della [**proprietà MsiLogFileLocation.**](msilogfilelocation.md)

## <a name="value"></a>Valore

Il valore di questa proprietà deve essere una stringa dei caratteri seguenti che specificano la modalità di registrazione predefinita.



| Valore                                                                        | Significato                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>Ho</dt> </dl> | Messaggi di stato.<br/>                                                    |
| <dl> <dt>w</dt> </dl> | Avvisi non irreversibile.<br/>                                                  |
| <dl> <dt>e</dt> </dl> | Tutti i messaggi di errore.<br/>                                                 |
| <dl> <dt>Un</dt> </dl> | Avviare le azioni.<br/>                                                |
| <dl> <dt>r</dt> </dl> | Record specifici dell'azione.<br/>                                            |
| <dl> <dt>u</dt> </dl> | Richieste dell'utente.<br/>                                                      |
| <dl> <dt>c</dt> </dl> | Parametri iniziali dell'interfaccia utente.<br/>                                              |
| <dl> <dt>m</dt> </dl> | Informazioni di uscita di memoria insufficiente o irreversibile.<br/>                            |
| <dl> <dt>o</dt> </dl> | Messaggi di spazio su disco insufficiente.<br/>                                         |
| <dl> <dt>P</dt> </dl> | Proprietà del terminale.<br/>                                                |
| <dl> <dt>v</dt> </dl> | Output dettagliato.<br/>                                                     |
| <dl> <dt>x</dt> </dl> | Informazioni di debug aggiuntive. Disponibile solo in Windows Server 2003.<br/> |
| <dl> <dt>!</dt> </dl> | Scaricare ogni riga nel log.<br/>                                         |



 

## <a name="remarks"></a>Commenti

Questa proprietà è disponibile a partire da Windows Installer 4.0.

Non è possibile usare i valori "+" \* e " " dell'opzione /L nel valore della proprietà **MsiLogging.**

La modalità di registrazione può essere impostata tramite criteri, un'opzione della riga di comando o a livello di codice. In questo modo viene eseguito l'override della modalità di registrazione predefinita. Per altre informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere [Registrazione](normal-logging.md) normale nella Windows [registrazione del](windows-installer-logging.md) programma di installazione.

Se la **proprietà MsiLogging** è presente nella tabella [Property](property-table.md), la modalità di registrazione predefinita del pacchetto può essere modificata modificando il valore di questa proprietà usando una trasformazione [del database](database-transforms.md). Non è possibile modificare la modalità di registrazione predefinita usando [un pacchetto patch](patch-packages.md) (un file con estensione msp).

Se la **proprietà MsiLogging** è stata impostata nella tabella Property [,](property-table.md)è possibile specificare la modalità di registrazione predefinita per tutti gli utenti del computer impostando i criteri [DisableLoggingFromPackage](disableloggingfrompackage.md) e [Logging.](logging.md) L'impostazione dei criteri DisableLoggingFromPackage e Dei criteri di registrazione eseguirà l'override **della proprietà MsiLogging** per tutti i pacchetti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 4.5 Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




