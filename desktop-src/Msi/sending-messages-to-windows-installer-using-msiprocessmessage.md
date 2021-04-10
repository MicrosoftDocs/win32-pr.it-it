---
description: I messaggi inviati tramite MsiProcessMessage sono gli stessi messaggi ricevuti dalla funzione di callback del \_ gestore INSTALLUI se è stato chiamato MsiSetExternalUI.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Inviare messaggi a Windows Installer tramite MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968577"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a>Invio di messaggi a Windows Installer tramite MsiProcessMessage

I messaggi inviati tramite [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) sono gli stessi messaggi ricevuti dalla funzione di callback [**del \_ gestore INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera) se è stato chiamato [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) . In caso contrario, Windows Installer gestisce i messaggi. Per informazioni dettagliate, vedere [analisi dei messaggi di Windows Installer](parsing-windows-installer-messages.md).

Ad esempio, per inviare un \_ messaggio di errore INSTALLMESSAGE con l' \_ icona MB ICONWARNING e i \_ pulsanti MB ABORTRETRYCANCEL:


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



Dove *hinstall* è l'handle per l'installazione, fornito a un'azione personalizzata o all'handle *hProduct* da [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) o [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)e *hRec* è il record contenente le informazioni sull'errore da formattare. Per informazioni sul modo in cui viene eseguita la formattazione, vedere [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).

Per impostazione predefinita, se \_ viene inviato un messaggio di errore INSTALLMESSAGE o INSTALLMESSAGE \_ FATALEXIT senza specificare tipi di pulsante o icone, MB \_ OK, nessuna icona e MB \_ DEFBUTTON1 vengono usati.

Windows Installer non assegna un'etichetta al pulsante **Interrompi** con la stringa "Abort" durante la visualizzazione di un MessageBox con la \_ specifica del pulsante MB AbortRetryIgnore (, invece contrassegna il pulsante con la stringa "Cancel". Tutti i messaggi di errore evitano di utilizzare la parola "Abort" e utilizzano invece la parola "Cancel".

Il parametro *hRecord* della funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) dipende dal tipo di messaggio inviato a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). Nell'elenco seguente vengono illustrati in dettaglio i requisiti del record in relazione al tipo di messaggio:

\_FATALEXIT INSTALLMESSAGE

 

\_informazioni INSTALLMESSAGE

 

\_OUTOFDISKSPACE INSTALLMESSAGE



| Campo         | Descrizione                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Modello per la formattazione della stringa risultante. Per ulteriori informazioni, vedere [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) . Si fa riferimento ai campi del record usando \[ 1 \] per il campo 1, \[ 2 \] per il campo 2 e così via. |
| da 1 a *n* | Tutti i campi successivi sono direttamente correlati ai campi a cui fa riferimento il modello nel campo 0.                                                                                                                    |



 

Se il campo 0 è null, la stringa ricevuta dal gestore dell'interfaccia utente viene formattata come: 1: \[ dati dal campo 1 \] 2: \[ dati dal campo 2 \] , ovvero per ogni campo del record, la stringa contiene il numero di campo seguito dai dati archiviati nel campo.

I messaggi informativi da [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) vengono registrati quando [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), l' [opzione della riga di comando](command-line-options.md)'/l ' o i [criteri di registrazione](logging.md) specificano le informazioni ' I ' o INSTALLLOGMODE \_ .

\_errore INSTALLMESSAGE

 

avviso di INSTALLMESSAGE \_

 

\_utente INSTALLMESSAGE

Per utilizzare un messaggio della tabella degli errori.



| Campo         | Descrizione                                           |
|---------------|-------------------------------------------------------|
| 0             | Deve essere null.                                         |
| 1             | Numero del messaggio nella [tabella degli errori](error-table.md). |
| da 2 a *n* | Correlato al messaggio specificato nella tabella degli errori.  |



 

Ad esempio,



| Campo | Tipo   | Data       |
|-------|--------|------------|
| 0     | string | Null       |
| 1     | INT    | 1304       |
| 2     | string | Myfile.txt |



 

Il messaggio risultante ricevuto dal gestore dell'interfaccia utente è:

Errore 1304. Errore durante la scrittura nel file: Myfile.txt. Verificare di disporre dell'accesso a tale directory.

Se il campo 0 non è null, viene eseguito l'override del messaggio della tabella degli errori. Al contrario, il modello Field 0 determina il formato del messaggio.

Il messaggio può inoltre specificare i pulsanti, incluso il pulsante predefinito, e l'icona da usare con il messaggio come indicato in precedenza. I tipi di pulsante e icona sono elencati [**nel \_ gestore INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera).

\_COMMONDATA INSTALLMESSAGE

Questo messaggio viene inviato per abilitare o disabilitare il pulsante **Annulla** in una finestra di dialogo di stato.



| Campo | Descrizione                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Non utilizzato.                                                                                                                                      |
| 1     | 2 si riferisce al pulsante **Annulla** .                                                                                                           |
| 2     | Il valore 1 indica che il pulsante **Annulla** deve essere visibile. Il valore 0 indica che il pulsante **Annulla** deve essere invisibile.<br/> |



 

Ad esempio, per disabilitare o nascondere il pulsante **Annulla** , il record verrebbe visualizzato come segue.



| Campo | Tipo   | Data |
|-------|--------|------|
| 0     | string | Null |
| 1     | INT    | 2    |
| 2     | INT    | 0    |



 

\_ACTIONSTART INSTALLMESSAGE

 

\_ACTIONDATA INSTALLMESSAGE

Il \_ record ACTIONSTART di INSTALLMESSAGE determina il formato del record ActionData.



| Campo | Descrizione                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| 0     | Null                                                                                                          |
| 1     | Nome dell'azione. Il nome in questo campo deve essere diverso da null.                                                         |
| 2     | Descrizione dell'azione.                                                                                           |
| 3     | Modello di azione. Viene usato per ActionData il cui messaggio viene formattato in base a questo modello. |



 

Non fare riferimento al campo 0 nel messaggio del modello di azione.

Il \_ record INSTALLMESSAGE ACTIONDATA è formattato come indicato di seguito.



| Campo         | Descrizione                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Null                                                                                                                                               |
| da 1 a *n* | Dipendente dal campo 3 del \_ messaggio o del modello INSTALLMESSAGE ACTIONSTART corrispondente specificato nella [tabella ActionText](actiontext-table.md). |



 

Ad esempio, il \_ record ACTIONSTART di INSTALLMESSAGE.



| Campo | Tipo   | Data                                                            |
|-------|--------|-----------------------------------------------------------------|
| 0     | string | Null                                                            |
| 1     | string | Azione                                                        |
| 2     | string | Questa è la descrizione di "azione"                           |
| 3     | string | Modello di azione: i dati di Field1 sono \[ 1 \] . i dati del campo 2 sono \[ 2 \] . |



 

Il modello per INSTALLMESSAGE \_ ACTIONSTART (Field 3) fa riferimento ai campi 1 e 2 \_ . il record INSTALLMESSAGE ACTIONDATA deve avere 2 campi contenenti i dati garantiti. I campi possono essere di tipo String o Integer.

\_Record ACTIONDATA INSTALLMESSAGE.



| Campo | Tipo   | Data                    |
|-------|--------|-------------------------|
| 0     | string | Null                    |
| 1     | INT    | 2                       |
| 2     | string | ActionData per l'azione |



 

filesinus INSTALLMESSAGE \_

Il record filesinus è un record di lunghezza variabile.



| Campo | Descrizione                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Questo campo può essere null. Per un'installazione mediante un'interfaccia utente di base, questo campo può specificare testo statico da visualizzare nel [controllo ListBox](listbox-control.md) della [finestra di dialogo filesinus](filesinuse-dialog.md). Per un'installazione che usa un'interfaccia utente completa, questo campo non ha alcun effetto perché il testo viene specificato dalla creazione della finestra di dialogo filesinusa personalizzata. |
| 1     | Nome del file in uso.                                                                                                                                                                                                                                                                                                                                        |
| 2     | Questo campo identifica il processo che contiene il file in uso. **Windows Installer versione 4,0:** ID processo (PID) del processo o titolo della finestra per il processo.<br/> **Windows Installer versione 3,1 e versioni precedenti:** Questo campo deve essere l'ID processo (PID) del processo.<br/>                                                      |



 

Ad esempio, per inviare un messaggio filesinus che mostra due file in uso, red.exe e blue.exe, il record ha quattro campi e il campo 0. Il formato del record sarà come illustrato nella tabella seguente. Questo esempio richiede Windows Installer versione 4,0.

**Windows Installer versione 3,1 e versioni precedenti:** I campi 2 e 4 nell'esempio seguente devono contenere i PID dei processi che mantengono red.exe e blue.exe in uso.



| Campo | Descrizione       |
|-------|-------------------|
| 0     | Null              |
| 1     | Red.exe           |
| 2     | Titolo della finestra rossa  |
| 3     | Blue.exe          |
| 4     | Titolo della finestra blu |



 

> [!Note]  
> In Windows Installer versione 4,0, se il PID passato dal servizio non ha un titolo della finestra, ad esempio un'applicazione della barra di sistema, il file non viene visualizzato e il log dettagliato contiene i messaggi seguenti.

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

\_RESOLVESOURCE INSTALLMESSAGE

Il \_ record RESOLVESOURCE di INSTALLMESSAGE include sette campi. Per \_ il corretto funzionamento di INSTALLMESSAGE RESOLVESOURCE, un gestore dell'interfaccia utente esterno potrebbe non gestire il \_ messaggio RESOLVESOURCE di INSTALLMESSAGE. Windows Installer necessario gestire il \_ messaggio INSTALLMESSAGE RESOLVESOURCE. Ovvero, il gestore dell'interfaccia utente esterno restituisce 0 per indicare che non viene eseguita alcuna azione quando si filtra il \_ messaggio INSTALLMESSAGE RESOLVESOURCE. La procedura consigliata consiste nell'evitare di inviare un messaggio RESOLVESOURCE.



| Campo | Descrizione                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Null                                                                                                                                                               |
| 1     | Null                                                                                                                                                               |
| 2     | Il nome del package.                                                                                                                                                      |
| 3     | Codice del prodotto.                                                                                                                                                      |
| 4     | Percorso relativo, se noto, può essere null.                                                                                                                               |
| 5     | 0                                                                                                                                                                  |
| 6     | Indica se convalidare il codice del pacchetto. Il valore ' 1' indica che il codice del pacchetto deve essere convalidato. Il valore ' 0' indica che il pacchetto non deve essere convalidato. |
| 7     | Disco richiesto dalla tabella dei supporti. Il valore ' 0' indica che qualsiasi disco è accettabile.                                                                              |



 

 

 




