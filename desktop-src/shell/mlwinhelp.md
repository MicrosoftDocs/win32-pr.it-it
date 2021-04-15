---
description: Avvia la Guida di Windows (Winhelp.exe) e passa dati aggiuntivi che indicano la natura della guida richiesta dall'applicazione.
ms.assetid: e7466832-f236-4567-b05d-37d25fe88ba2
title: MLWinHelp (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLWinHelp
- MLWinHelpA
- MLWinHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: badfeb599fd24fd255eb064bbaf6d99a3b758bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977887"
---
# <a name="mlwinhelp-function"></a>MLWinHelp (funzione)

\[Questa funzione è disponibile tramite Windows XP e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Avvia la Guida di Windows (Winhelp.exe) e passa dati aggiuntivi che indicano la natura della guida richiesta dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL MLWinHelp(
  _In_ HWND      hWndMain,
  _In_ LPCTSTR   lpszHelp,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hWndMain* \[ in\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra che richiede la guida. La funzione **MLWinHelp** usa questo handle per tenere traccia delle applicazioni che hanno richiesto la guida. Se il parametro *uCommand* specifica Help \_ ContextMenu o Help \_ WM \_ Help, *hWndMain* identifica il controllo che richiede la guida.

</dd> <dt>

*lpszHelp* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR**

Indirizzo di una stringa con terminazione null contenente il percorso, se necessario, e il nome del file della guida che **MLWinHelp** deve visualizzare.

Il nome del file può essere seguito da una parentesi angolare (>) e dal nome di una finestra secondaria se l'argomento deve essere visualizzato in una finestra secondaria anziché nella finestra primaria. È necessario definire il nome della finestra secondaria nella \[ \] sezione Windows del file del progetto della guida (. hpj).

</dd> <dt>

*uCommand* \[ in\]
</dt> <dd>

Tipo: **uint**

Tipo di guida richiesto. Per un elenco dei valori possibili e il modo in cui influiscono sul valore da inserire nel parametro *dwData* , vedere la sezione Osservazioni.

</dd> <dt>

*dwData* \[ in\]
</dt> <dd>

Tipo: **DWORD \_ ptr**

Dati aggiuntivi. Il valore utilizzato dipende dal valore del parametro *uCommand* . Per un elenco dei valori *dwData* possibili, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Restituisce un valore diverso da zero in caso di esito positivo o zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Questa funzione non è inclusa in un file di intestazione e deve essere chiamata dall'ordinale 395 per **MLWinHelpA** e 397 per **MLWinHelpW**.

**MLWinHelp** è essenzialmente un wrapper per [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Tenta di ottenere il percorso del file della Guida corrispondente all'impostazione della lingua dell'interfaccia utente corrente prima di chiamare **WinHelp**. Se ha esito positivo, passa il percorso. Se ha esito negativo, passa il percorso a cui punta *lpszHelp*.

Questa funzione ha esito negativo se viene chiamata da qualsiasi contesto ma dall'utente corrente.

Prima di chiudere la finestra che ha richiesto la guida, l'applicazione deve chiamare **MLWinHelp** con il set di parametri *uCommand* per consentire l' \_ uscita. Finché tutte le applicazioni non hanno eseguito questa operazione, la Guida di Windows non verrà terminata. Si noti che non è necessario chiamare la Guida di Windows con il \_ comando help Quit se è stato usato il \_ comando help CONTEXTPOPUP per avviare la Guida di Windows.

Nella tabella seguente vengono illustrati i valori possibili per il parametro *uCommand* e i formati corrispondenti del parametro *dwData* .



| *uCommand*          | Azione                                                                                                                                                                                                                                                               | *dwData*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| comando della Guida \_       | Esegue una macro della guida o una stringa macro.                                                                                                                                                                                                                               | Indirizzo di una stringa che specifica il nome delle macro della guida da eseguire. Se la stringa specifica più nomi di macro, i nomi devono essere separati da punti e virgola. È necessario utilizzare la forma abbreviata del nome della macro per alcune macro perché la Guida di Windows non supporta il nome lungo.                         |
| contenuto della Guida \_      | Visualizza l'argomento specificato dall'opzione Contents nella \[ sezione Options \] del file con estensione HPJ. Questo comando è per compatibilità con le versioni precedenti. Le nuove applicazioni devono fornire un file con estensione cnt e usare il \_ comando Help Finder.                                           | Ignorato impostare su 0.                                                                                                                                                                                                                                                                                           |
| contesto della Guida \_       | Visualizza l'argomento identificato dall'identificatore di contesto specificato definito nella \[ \] sezione della mappa del file con estensione HPJ.                                                                                                                                                   | Contiene l'identificatore di contesto per l'argomento.                                                                                                                                                                                                                                                               |
| ContextMenu della Guida \_   | Consente di visualizzare il menu della **Guida** per la finestra selezionata, quindi di visualizzare l'argomento relativo al controllo selezionato in una finestra popup.                                                                                                                                             | Indirizzo di una matrice di coppie **DWORD** . Il primo **DWORD** in ogni coppia è l'identificatore del controllo, mentre il secondo è l'identificatore di contesto per l'argomento. La matrice deve terminare con una coppia di zeri {0,0} . Se non si desidera aggiungere la guida a un particolare controllo, impostare il relativo identificatore di contesto su-1. |
| Guida \_ CONTEXTPOPUP  | Visualizza l'argomento identificato dall'identificatore di contesto specificato definito nella \[ \] sezione della mappa del file con estensione HPJ in una finestra popup.                                                                                                                                | Contiene l'identificatore di contesto per un argomento.                                                                                                                                                                                                                                                                 |
| ricerca della Guida \_        | Consente di visualizzare la finestra di dialogo **argomenti della Guida** .                                                                                                                                                                                                                             | Ignorato impostare su 0.                                                                                                                                                                                                                                                                                           |
| Guida \_ FORCEFILE     | Garantisce che la Guida di Windows visualizzi il file della Guida corretto. Se viene visualizzato il file della Guida errato, viene visualizzata la Guida di Windows corretta. in caso contrario, non viene eseguita alcuna azione.                                                                                     | Ignorato impostare su 0.                                                                                                                                                                                                                                                                                           |
| Guida \_ HELPONHELP    | Visualizza la guida su come utilizzare la Guida di Windows, se il file Winhlp32. hlp è disponibile.                                                                                                                                                                                     | Ignorato impostare su 0.                                                                                                                                                                                                                                                                                           |
| Indice della Guida \_         | Visualizza l'argomento specificato dall'opzione Contents nella \[ sezione Options \] del file con estensione HPJ. Questo comando è per compatibilità con le versioni precedenti. Le nuove applicazioni devono usare il \_ comando Help Finder.                                                                   | Ignorato impostare su 0.                                                                                                                                                                                                                                                                                           |
| chiave della Guida \_           | Visualizza l'argomento nella tabella delle parole chiave che corrisponde alla parola chiave specificata, se esiste una corrispondenza esatta. Se è presente più di una corrispondenza, Visualizza l'indice con gli argomenti elencati nella casella di riepilogo **argomenti trovati** .                                                 | Indirizzo di una stringa di parola chiave. Più parole chiave devono essere separate da punti e virgola.                                                                                                                                                                                                                              |
| Guida \_ join      | Visualizza l'argomento specificato da una parola chiave in una tabella di parole chiave alternative.                                                                                                                                                                                           | Indirizzo di una struttura [**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) che specifica un carattere a piè di pagina e una parola chiave.                                                                                                                                                                                     |
| Guida \_ PARTIALKEY    | Visualizza l'argomento nella tabella delle parole chiave che corrisponde alla parola chiave specificata, se esiste una corrispondenza esatta. Se è presente più di una corrispondenza, Visualizza la finestra di dialogo **argomenti trovati** . Per visualizzare l'indice senza passare una parola chiave, usare un puntatore a una stringa vuota. | Indirizzo di una stringa di parola chiave. Più parole chiave devono essere separate da punti e virgola.                                                                                                                                                                                                                              |
| Guida \_ uscita          | Informa la Guida di Windows che non è più necessaria. Se nessun'altra applicazione richiede assistenza, Windows chiude la Guida di Windows.                                                                                                                                         | Ignorato impostare su 0.                                                                                                                                                                                                                                                                                           |
| Guida ai \_ contenuti   | Specifica l'argomento relativo al contenuto. La Guida di Windows Visualizza questo argomento quando l'utente fa clic sul pulsante **contenuto** se al file della guida non è associato un file con estensione cnt.                                                                                                  | Contiene l'identificatore di contesto per l'argomento relativo al contenuto.                                                                                                                                                                                                                                                      |
| HELP \_ sepopup \_ pos | Imposta la posizione della finestra popup successiva.                                                                                                                                                                                                                   | Contiene i dati di posizione. Usare la macro [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) per concatenare le coordinate orizzontali e verticali in un singolo valore. La finestra popup viene posizionata come se il cursore del mouse si trovasse in corrispondenza del punto specificato quando era richiamata la finestra popup.                                 |
| Guida \_ SETWINPOS     | Visualizza la finestra della Guida di Windows, se è ridotta a icona o in memoria, e ne imposta la dimensione e la posizione come specificato.                                                                                                                                                      | Indirizzo di una struttura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) che specifica le dimensioni e la posizione di una finestra della guida primaria o secondaria.                                                                                                                                                             |
| Guida \_ TCARD         | Indica che un comando è relativo a un'istanza della scheda di training della Guida di Windows. Combinare questo comando con altri comandi usando l'operatore OR bit per bit.                                                                                                                    | Dipende dal comando con cui viene combinato questo comando.                                                                                                                                                                                                                                                  |
| Guida di \_ WM \_      | Visualizza l'argomento relativo al controllo identificato dal parametro *hWndMain* in una finestra popup.                                                                                                                                                                        | Indirizzo di una matrice di coppie **DWORD** . Il primo **DWORD** in ogni coppia è un identificatore di controllo, mentre il secondo è un identificatore di contesto per un argomento. La matrice deve terminare con una coppia di zeri {0,0} . Se non si desidera aggiungere la guida a un particolare controllo, impostare il relativo identificatore di contesto su-1.       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **MLWinHelpW** (Unicode) e **MLWinHelpA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
