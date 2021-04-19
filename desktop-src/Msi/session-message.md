---
description: Il Metodo Message dell'oggetto Session esegue tutte le operazioni di registrazione abilitate e rinvia l'esecuzione all'oggetto gestore dell'interfaccia utente associato al motore. La registrazione può essere abilitata selettivamente per i vari tipi di messaggio. Vedere il metodo EnableLog.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session. Message, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333051"
---
# <a name="sessionmessage-method"></a>Session. Message, metodo

Il metodo **Message** dell'oggetto [**Session**](session-object.md) esegue tutte le operazioni di registrazione abilitate e rinvia l'esecuzione all'oggetto gestore dell'interfaccia utente associato al motore. La registrazione può essere abilitata selettivamente per i vari tipi di messaggio. Vedere il metodo [**EnableLog**](installer-enablelog.md) .

Se il campo record 0 contiene una stringa di formattazione, viene usato per formattare i dati negli altri campi. In caso contrario, se il messaggio è un errore, un avviso o un messaggio utente, viene effettuato un tentativo di trovare un modello di messaggio nella tabella degli errori per il database corrente utilizzando il numero di errore trovato nel campo 1 del record per i tipi di messaggio e i valori restituiti.

## <a name="syntax"></a>Sintassi


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo* 
</dt> <dd>

Il parametro *Kind* è obbligatorio per uno dei valori seguenti. Per visualizzare una finestra di messaggio con pulsanti e icone di push, calcolare il valore di *Kind* aggiungendo gli stili standard della finestra di messaggio utilizzati da [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) e [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) a **msiMessageTypeError**, **msiMessageTypeWarning** o **msiMessageTypeUser**. Per ulteriori informazioni, vedere la sezione Osservazioni riportata di seguito.



| Costante                                                                                                                                                                                                                                                                                                                 | Significato                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt> </dl>                     | Terminazione prematura, probabilmente insufficiente.<br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt> </dl>                                     | Messaggio di errore formattato, \[ 1 \] indica il numero del messaggio nella [tabella degli errori](error-table.md).<br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt> </dl>                             | Messaggio di avviso formattato, \[ 1 \] indica il numero del messaggio nella [tabella degli errori](error-table.md).<br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt> </dl>                                     | Messaggio di richiesta dell'utente, \[ 1 \] indica il numero del messaggio nella [tabella degli errori](error-table.md).<br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt> </dl>                                         | Messaggio informativo per il log, che non deve essere visualizzato.<br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt> </dl>                 | Elenco di file in uso che devono essere sostituiti.<br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt> </dl>     | Richiesta per determinare un percorso di origine valido.<br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt> </dl> | Messaggio di spazio su disco insufficiente.<br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt> </dl>             | Inizio dell'azione, \[ 1 \] nome azione, \[ 2 \] Descrizione, \[ 3 \] modello per i messaggi ACTIONDATA.<br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt> </dl>                 | Dati dell'azione. I campi dei record corrispondono al modello del messaggio ACTIONSTART.<br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt> </dl>                         | Informazioni sull'indicatore di stato. Vedere la descrizione dei campi di record riportati di seguito.<br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt> </dl>             | Per abilitare il pulsante Annulla \[ , impostare 1 \] su 2 e \[ 2 \] su 1. <br/> Per disabilitare il pulsante Annulla \[ , impostare 1 \] su 2 e \[ 2 \] su 0<br/> |



 

</dd> <dt>

*record* 
</dt> <dd>

Oggetto [**record**](record-object.md) obbligatorio contenente un campo specifico del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Costante                                                                                              | Valore         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <dt>**msiMessageStatusError**</dt> </dl>  | -1<br/> |
| <dl> <dt>**msiMessageStatusNone**</dt> </dl>   | 0<br/>  |
| <dl> <dt>**msiMessageStatusOk**</dt> </dl>     | 1<br/>  |
| <dl> <dt>**msiMessageStatusCancel**</dt> </dl> | 2<br/>  |
| <dl> <dt>**msiMessageStatusAbort**</dt> </dl>  | 3<br/>  |
| <dl> <dt>**msiMessageStatusRetry**</dt> </dl>  | 4<br/>  |
| <dl> <dt>**msiMessageStatusIgnore**</dt> </dl> | 5<br/>  |
| <dl> <dt>**msiMessageStatusYes**</dt> </dl>    | 6<br/>  |
| <dl> <dt>**msiMessageStatusNo**</dt> </dl>     | 7<br/>  |



 

## <a name="remarks"></a>Commenti

**Campi di record del messaggio**

Di seguito vengono descritte le definizioni dei campi di record quando msiMessageTypeProgress viene passato come tipo di messaggio.

Field 1 specifica il tipo del messaggio di stato. Il significato degli altri campi dipende dal valore in questo campo. I valori possibili che è possibile impostare nel campo 1 sono i seguenti.



| Nome messaggio     | Valore | Descrizione campo 1                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| MasterReset      | 0     | Reimposta l'indicatore di stato e imposta il numero totale previsto di cicli sulla barra.                                         |
| ActionInfo       | 1     | Fornisce informazioni correlate ai messaggi di stato che devono essere inviati dall'azione corrente.                                 |
| ProgressReport   | 2     | Incrementa l'indicatore di stato.                                                                                        |
| ProgressAddition | 3     | Abilita un'azione (ad esempio CustomAction) per aggiungere i segni di avanzamento al numero totale previsto di stato dell'indicatore di stato. |



 

Il significato del campo 2 dipende dal valore nel campo 1, come indicato di seguito.



| Valore campo 1 | Descrizione campo 2                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| 0             | Previsto numero totale di cicli nell'indicatore di stato.                                                        |
| 1             | Numero di cicli di selezione dell'indicatore di stato per ogni messaggio ActionData. Questo campo viene ignorato se il campo 3 è 0. |
| 2             | Numero di cicli spostati nell'indicatore di stato.                                                                |
| 3             | Numero di cicli da aggiungere allo stato di avanzamento previsto totale.                                                         |



 

Il significato del campo 3 dipende dal valore nel campo 1, come indicato di seguito.



| Valore campo 1 | Valore campo 3 | Descrizione campo 3                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| 0             | 0             | Indicatore di stato avanti (da sinistra a destra)                                                                            |
|               | 1             | Barra di avanzamento indietro (da destra a sinistra)                                                                           |
| 1             | 0             | L'azione corrente invierà messaggi ProgressReport espliciti.                                                  |
|               | 1             | Incrementare l'indicatore di stato in base al numero di cicli specificati nel campo 2 ogni volta che viene inviato un messaggio ActionData. |
| 2             | Non utilizzato        |                                                                                                                 |
| 3             | Non utilizzato        |                                                                                                                 |



 

Il significato del campo 4 dipende dal valore nel campo 1, come indicato di seguito.



| Valore campo 1 | Valore campo 4 | Descrizione campo 4                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | 0             | Esecuzione in corso. In questo caso, l'interfaccia utente potrebbe calcolare e visualizzare il tempo rimanente.                                                      |
|               | 1             | Creazione dello script di esecuzione. In questo caso, l'interfaccia utente potrebbe visualizzare un messaggio per attendere il completamento della preparazione dell'installazione da parte del programma di installazione. |
| 1             | Non utilizzato        |                                                                                                                                                     |
| 2             | Non utilizzato        |                                                                                                                                                     |
| 3             | Non utilizzato        |                                                                                                                                                     |



 

**Visualizzazione di finestre di messaggio**

Per visualizzare una finestra di messaggio con pulsanti e icone di push, calcolare il valore di *Kind* aggiungendo gli stili standard della finestra di messaggio utilizzati da **MessageBox** e **MessageBoxEx** a **msiMessageTypeError**, **msiMessageTypeWarning** o **msiTypeUser**. Le opzioni disponibili per i pulsanti di push per VBScript sono vbOKOnly (MB \_ OK), vbOKCancel (MB \_ OKCANCEL), VBABORTRETRYIGNORE (MB \_ AbortRetryIgnore (), vbYesNoCancel (MB \_ YESNOCANCEL), vbYesNo (MB \_ YesNo) e vbRetryCancel (MB \_ RETRYCANCEL). Le opzioni delle icone disponibili per VBScript sono vbCritical (MB \_ ICONERROR), vbQuestion (MB \_ ICONQUESTION), VBEXCLAMATION (MB \_ ICONWARNING) e vbInformation (MB \_ ICONINFORMATION).

Ad esempio, la chiamata seguente invia un messaggio **msiMessageTypeError** con l'icona vbExclamation e i pulsanti vbYesNo.


```VB
Session.Message &H01000034, record
```



Se un'azione personalizzata chiama il metodo del **messaggio** , l'azione personalizzata deve essere in grado di gestire un annullamento da parte dell'utente e deve restituire **msiDoActionStatusUserExit**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 
