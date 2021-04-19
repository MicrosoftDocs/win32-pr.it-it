---
description: La proprietà MsiLogging imposta la modalità di registrazione predefinita per il pacchetto di Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Proprietà MsiLogging
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332615"
---
# <a name="msilogging-property"></a>Proprietà MsiLogging

La proprietà **MsiLogging** imposta la modalità di registrazione predefinita per il pacchetto di Windows Installer. Se questa proprietà facoltativa è presente nella [tabella delle proprietà](property-table.md), il programma di installazione genera un file di log denominato MSI \* . LOG. Il percorso completo del file di log viene fornito dal valore della proprietà [**MsiLogFileLocation**](msilogfilelocation.md) .

## <a name="value"></a>Valore

Il valore di questa proprietà deve essere una stringa dei caratteri seguenti che specificano la modalità di registrazione predefinita.



| Valore                                                                        | Significato                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>I</dt> </dl> | Messaggi di stato.<br/>                                                    |
| <dl> <dt>w</dt> </dl> | Avvisi non irreversibili.<br/>                                                  |
| <dl> <dt>e</dt> </dl> | Tutti i messaggi di errore.<br/>                                                 |
| <dl> <dt>un</dt> </dl> | Avvio delle azioni.<br/>                                                |
| <dl> <dt>r</dt> </dl> | Record specifici dell'azione.<br/>                                            |
| <dl> <dt>u</dt> </dl> | Richieste dell'utente.<br/>                                                      |
| <dl> <dt>c</dt> </dl> | Parametri iniziali dell'interfaccia utente.<br/>                                              |
| <dl> <dt>m</dt> </dl> | Informazioni sulla memoria insufficiente o sull'uscita fatale.<br/>                            |
| <dl> <dt>o</dt> </dl> | Messaggi di spazio fuori disco.<br/>                                         |
| <dl> <dt>p</dt> </dl> | Proprietà del terminale.<br/>                                                |
| <dl> <dt>v</dt> </dl> | Output dettagliato.<br/>                                                     |
| <dl> <dt>x</dt> </dl> | Informazioni di debug aggiuntive. Disponibile solo in Windows Server 2003.<br/> |
| <dl> <dt>!</dt> </dl> | Scaricare ogni riga nel log.<br/>                                         |



 

## <a name="remarks"></a>Commenti

Questa proprietà è disponibile a partire da Windows Installer 4,0.

Non è possibile usare i valori "+" e " \* " dell'opzione/l nel valore della proprietà **MsiLogging** .

La modalità di registrazione può essere impostata tramite criteri, un'opzione della riga di comando o a livello di codice. Viene eseguito l'override della modalità di registrazione predefinita. Per ulteriori informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere [registrazione normale](normal-logging.md) nella sezione [registrazione Windows Installer](windows-installer-logging.md) .

Se la proprietà **MsiLogging** è presente nella [tabella delle proprietà](property-table.md), è possibile modificare la modalità di registrazione predefinita del pacchetto modificando il valore di questa proprietà utilizzando una [trasformazione del database](database-transforms.md). Non è possibile modificare la modalità di registrazione predefinita utilizzando un [pacchetto di patch](patch-packages.md) , ovvero un file con estensione msp.

Se la proprietà **MsiLogging** è stata impostata nella [tabella delle proprietà](property-table.md), è possibile specificare la modalità di registrazione predefinita per tutti gli utenti del computer impostando il criterio [DisableLoggingFromPackage](disableloggingfrompackage.md) e i criteri di [registrazione](logging.md) . L'impostazione del criterio DisableLoggingFromPackage e dei criteri di registrazione eseguirà l'override della proprietà **MsiLogging** per tutti i pacchetti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 4,5 in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




