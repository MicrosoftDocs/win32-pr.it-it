---
description: I messaggi inviati tramite MsiProcessMessage sono gli stessi messaggi ricevuti dalla funzione di callback INSTALLUI HANDLER se è stato chiamato \_ MsiSetExternalUI.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Inviare messaggi a Windows programma di installazione tramite MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1c639e45b22c2406f446ab31072ceb02ab9b3e906f5973b1436356d96f3782
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629951"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a>Invio di messaggi a Windows programma di installazione tramite MsiProcessMessage

I messaggi inviati tramite [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) sono gli stessi messaggi ricevuti dalla funzione di callback [**INSTALLUI \_ HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera) se è stato chiamato [**MsiSetExternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) In caso contrario, Windows installer gestisce i messaggi. Per informazioni dettagliate, vedere [Analisi dei Windows del programma di installazione.](parsing-windows-installer-messages.md)

Ad esempio, per inviare un messaggio di errore INSTALLMESSAGE con l'icona MBICONA IN CORSO e i pulsanti \_ \_ MB \_ ABORTRETRYCANCEL:


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



Dove *hInstall* è l'handle per l'installazione, fornito a un'azione personalizzata o all'handle *hProduct* da [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) o [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)e *hRec* è il record contenente le informazioni sull'errore da formattare. Per informazioni su come viene eseguita la formattazione, [**vedere MsiFormatRecord.**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

Per impostazione predefinita, se viene inviato un messaggio INSTALLMESSAGE ERROR o INSTALLMESSAGE FATALEXIT senza specificare il tipo di pulsante o i tipi di icona, vengono usati MB OK, nessuna icona e \_ \_ MB \_ \_ DEFBUTTON1.

Windows Il programma di installazione non etichetta il pulsante **ABORT** con la stringa "Abort" quando viene visualizzato un MessageBox con la specifica del pulsante MB ABORTRETRYIGNORE, ma etichetta il pulsante con la stringa \_ "Cancel". Tutti i messaggi di errore evitano di usare la parola "Abort" e usano invece la parola "Cancel".

Il *parametro hRecord* della [**funzione MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) dipende dal tipo di messaggio inviato a [**MsiProcessMessage.**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) L'elenco seguente indica in dettaglio i requisiti del record in relazione al tipo di messaggio:

INSTALLMESSAGE \_ FATALEXIT

 

INSTALLMESSAGE \_ INFO

 

INSTALLMESSAGE \_ OUTOFDISKSPACE



| Campo         | Descrizione                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Modello per la formattazione della stringa risultante. Per [**altre informazioni, vedere MsiFormatRecord.**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) Viene fatto riferimento ai campi del record usando \[ 1 \] per il campo 1, \[ 2 per il campo \] 2 e così via. |
| Da 1 a *n* | Tutti i campi successivi sono direttamente correlati ai campi a cui fa riferimento il modello nel campo 0.                                                                                                                    |



 

Se il campo 0 è Null, la stringa ricevuta dal gestore dell'interfaccia utente viene formattata come: 1: dati dal campo 1 2: dati del campo 2, vale a dire che per ogni campo del record la stringa contiene il numero di campo seguito dai dati archiviati \[ \] nel \[ \] campo.

I messaggi informativi [**da MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) vengono registrati quando [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), [](logging.md) l'opzione della riga di comando '/l' [](command-line-options.md)o i criteri di registrazione specificano 'I' o INSTALLLOGMODE \_ INFO.

ERRORE \_ INSTALLMESSAGE

 

AVVISO \_ INSTALLMESSAGE

 

INSTALLMESSAGE \_ USER

Per utilizzare un messaggio della tabella Error.



| Campo         | Descrizione                                           |
|---------------|-------------------------------------------------------|
| 0             | Deve essere Null.                                         |
| 1             | Numero di messaggio nella [tabella Degli errori](error-table.md). |
| Da 2 a *n* | Correlato al messaggio specificato nella tabella Error.  |



 

Ad esempio,



| Campo | Tipo   | Dati       |
|-------|--------|------------|
| 0     | string | Null       |
| 1     | int    | 1304       |
| 2     | string | Myfile.txt |



 

Il messaggio risultante ricevuto dal gestore dell'interfaccia utente è:

Errore 1304. Errore durante la scrittura nel file: Myfile.txt. Verificare di avere accesso a tale directory.

Se il campo 0 non è Null, viene eseguito l'override del messaggio della tabella degli errori. Il modello di campo 0 determina invece il formato del messaggio.

Il messaggio può anche specificare i pulsanti, tra cui il pulsante predefinito e l'icona da usare con il messaggio, come indicato in precedenza. I tipi di pulsante e icona sono elencati in [**INSTALLUI \_ HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera).

INSTALLMESSAGE \_ COMMONDATA

Questo messaggio viene inviato per abilitare o disabilitare il **pulsante** Annulla in una finestra di dialogo di stato.



| Campo | Descrizione                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non utilizzato.                                                                                                                                      |
| 1     | 2 fa riferimento al **pulsante** Annulla.                                                                                                           |
| 2     | Il valore 1 indica che il **pulsante** Annulla deve essere visibile. Il valore 0 indica che il **pulsante Annulla** deve essere invisibile.<br/> |



 

Ad esempio, per disabilitare o nascondere il **pulsante** Annulla, il record verrà visualizzato come segue.



| Campo | Tipo   | Dati |
|-------|--------|------|
| 0     | string | Null |
| 1     | int    | 2    |
| 2     | INT    | 0    |



 

INSTALLMESSAGE \_ ACTIONSTART

 

INSTALLMESSAGE \_ ACTIONDATA

Il record INSTALLMESSAGE \_ ACTIONSTART determina il formato del record ActionData.



| Campo | Descrizione                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| 0     | Null                                                                                                          |
| 1     | Nome dell'azione. Il nome in questo campo deve essere diverso da Null.                                                         |
| 2     | Descrizione dell'azione.                                                                                           |
| 3     | Modello di azione. Viene usato per ActionData il cui messaggio viene formattato in base a questo modello. |



 

Non fare riferimento al campo 0 nel messaggio del modello di azione.

Il record INSTALLMESSAGE \_ ACTIONDATA viene formattato come segue.



| Campo         | Descrizione                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Null                                                                                                                                               |
| Da 1 a *n* | Dipende dal campo 3 del messaggio o del modello INSTALLMESSAGE ACTIONSTART corrispondente \_ specificato nella tabella [ActionText](actiontext-table.md). |



 

Ad esempio, il record INSTALLMESSAGE \_ ACTIONSTART.



| Campo | Tipo   | Dati                                                            |
|-------|--------|-----------------------------------------------------------------|
| 0     | string | Null                                                            |
| 1     | string | MyAction                                                        |
| 2     | string | Questa è la descrizione di "MyAction"                           |
| 3     | string | Modello MyAction: i dati field1 sono \[ 1 \] . I dati del campo 2 sono \[ 2 \] . |



 

Il modello per INSTALLMESSAGE ACTIONSTART (campo 3) fa riferimento ai campi 1 e 2. Il record INSTALLMESSAGE ACTIONDATA deve avere 2 campi contenenti i \_ \_ dati garantiti. I campi possono essere di tipo stringa o integer.

InstallMESSAGE \_ ACTIONDATA.



| Campo | Tipo   | Dati                    |
|-------|--------|-------------------------|
| 0     | string | Null                    |
| 1     | int    | 2                       |
| 2     | string | ActionData per MyAction |



 

INSTALLMESSAGE \_ FILESINUSE

Il record FILESINUSE è un record a lunghezza variabile.



| Campo | Descrizione                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Questo campo può essere Null. Per un'installazione che usa un'interfaccia utente di base, questo campo può specificare testo statico da visualizzare nel controllo [ListBox](listbox-control.md) della [finestra di dialogo FilesInUse](filesinuse-dialog.md). Per un'installazione che usa un'interfaccia utente completa, questo campo non ha alcun effetto perché il testo viene specificato dalla creazione della finestra di dialogo Personalizzata FilesInUse. |
| 1     | Nome del file in uso.                                                                                                                                                                                                                                                                                                                                        |
| 2     | Questo campo identifica il processo che contiene il file in uso. **Windows Installer versione 4.0:** ID processo (PID) del processo o titolo della finestra per il processo.<br/> **Windows Installer versione 3.1 e precedenti:** Questo campo deve essere l'ID processo (PID) del processo.<br/>                                                      |



 

Ad esempio, per inviare un messaggio FilesInUse che mostra due file in uso, red.exe e blue.exe, il record ha quattro campi più il campo 0. Il formato del record sarà come illustrato nella tabella seguente. Questo esempio richiede Windows Installer versione 4.0.

**Windows Installer versione 3.1 e precedenti:** I campi 2 e 4 nell'esempio seguente devono contenere i PIN dei processi che red.exe e blue.exe in uso.



| Campo | Descrizione       |
|-------|-------------------|
| 0     | Null              |
| 1     | Red.exe           |
| 2     | Titolo della finestra rossa  |
| 3     | Blue.exe          |
| 4     | Titolo della finestra blu |



 

> [!Note]  
> In Windows Installer versione 4.0, se il PID passato dal servizio non ha un titolo di finestra, ad esempio un'applicazione dell'area di notifica, il file non viene visualizzato e il log dettagliato contiene i messaggi seguenti.

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

INSTALLMESSAGE \_ RESOLVESOURCE

Il record INSTALLMESSAGE \_ RESOLVESOURCE include sette campi. Per il corretto funzionamento di INSTALLMESSAGE RESOLVESOURCE, un gestore dell'interfaccia utente esterno potrebbe non \_ gestire il messaggio INSTALLMESSAGE \_ RESOLVESOURCE. Windows Il programma di installazione deve gestire il messaggio INSTALLMESSAGE \_ RESOLVESOURCE. Ciò significa che il gestore dell'interfaccia utente esterno restituisce 0 per indicare che non è stata eseguita alcuna azione quando si filtra il messaggio INSTALLMESSAGE \_ RESOLVESOURCE. La procedura consigliata consiste nell'evitare l'invio di un messaggio RESOLVESOURCE.



| Campo | Descrizione                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Null                                                                                                                                                               |
| 1     | Null                                                                                                                                                               |
| 2     | Il nome del package.                                                                                                                                                      |
| 3     | Codice prodotto.                                                                                                                                                      |
| 4     | Il percorso relativo, se noto, può essere Null.                                                                                                                               |
| 5     | 0                                                                                                                                                                  |
| 6     | Se convalidare il codice del pacchetto. Il valore "1" indica che il codice del pacchetto deve essere convalidato. Il valore '0' indica che il pacchetto non deve essere convalidato. |
| 7     | Disco richiesto dalla tabella dei supporti. Il valore "0" indica che qualsiasi disco è accettabile.                                                                              |



 

 

 




