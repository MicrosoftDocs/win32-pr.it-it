---
description: Avvia Windows guida (Winhelp.exe) e passa dati aggiuntivi che indicano la natura della Guida richiesta dall'applicazione.
ms.assetid: e7466832-f236-4567-b05d-37d25fe88ba2
title: Funzione MLWinHelp
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
ms.openlocfilehash: a6c109f39107ba3cfd1800cca8db516d0033a2f3c32b9784e4359b3c6c50655d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968900"
---
# <a name="mlwinhelp-function"></a>Funzione MLWinHelp

\[Questa funzione è disponibile tramite Windows XP e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Avvia Windows guida (Winhelp.exe) e passa dati aggiuntivi che indicano la natura della Guida richiesta dall'applicazione.

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

*hWndMain* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra che richiede assistenza. La **funzione MLWinHelp** usa questo handle per tenere traccia delle applicazioni che hanno richiesto assistenza. Se il *parametro uCommand* specifica HELP \_ CONTEXTMENU o HELP \_ WM \_ HELP, *hWndMain* identifica il controllo che richiede assistenza.

</dd> <dt>

*lpszHelp* \[ Pollici\]
</dt> <dd>

Tipo: **LPCTSTR**

Indirizzo di una stringa con terminazione Null contenente il percorso, se necessario, e il nome del file della Guida che **MLWinHelp** deve visualizzare.

Il nome del file può essere seguito da una parentesi uncinata (>) e dal nome di una finestra secondaria se l'argomento deve essere visualizzato in una finestra secondaria anziché nella finestra primaria. È necessario definire il nome della finestra secondaria nella sezione WINDOWS del file del progetto della Guida \[ \] (con estensione hpj).

</dd> <dt>

*uCommand* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Tipo di guida richiesta. Per un elenco dei valori possibili e il modo in cui influiscono sul valore da inserire nel *parametro dwData,* vedere la sezione Osservazioni.

</dd> <dt>

*dwData* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD \_ PTR**

Dati aggiuntivi. Il valore usato dipende dal valore del *parametro uCommand.* Per un elenco dei *possibili valori dwData,* vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **BOOL**

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Questa funzione non è inclusa in un file di intestazione e deve essere chiamata dagli ordinali 395 per **MLWinHelpA** e 397 **per MLWinHelpW.**

**MLWinHelp** è essenzialmente un wrapper per [**WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Tenta di ottenere il percorso del file della Guida corrispondente all'impostazione della lingua dell'interfaccia utente corrente prima di **chiamare WinHelp.** Se ha esito positivo, passa tale percorso. Se ha esito negativo, passa il percorso a cui punta *lpszHelp*.

Questa funzione ha esito negativo se viene chiamata da qualsiasi contesto, ma dall'utente corrente.

Prima di chiudere la finestra che ha richiesto la Guida, l'applicazione deve chiamare **MLWinHelp** con il *parametro uCommand* impostato su HELP \_ QUIT. Fino a quando tutte le applicazioni non hanno eseguito questa operazione, Windows guida non verrà terminata. Si noti che la Windows guida con il comando HELP QUIT non è necessaria se è stato usato il comando \_ HELP CONTEXTPOPUP per avviare Windows \_ Guida.

La tabella seguente illustra i valori possibili per *il parametro uCommand* e i formati corrispondenti del *parametro dwData.*



| *uCommand*          | Azione                                                                                                                                                                                                                                                               | *dwData*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMANDO \_ HELP       | Esegue una macro della Guida o una stringa di macro.                                                                                                                                                                                                                               | Indirizzo di una stringa che specifica il nome delle macro della Guida da eseguire. Se la stringa specifica più nomi di macro, i nomi devono essere separati da punti e virgola. È necessario usare la forma abbreviata del nome della macro per alcune macro perché Windows guida non supporta il nome lungo.                         |
| CONTENUTO DELLA \_ GUIDA      | Visualizza l'argomento specificato dall'opzione Contenuto nella \[ sezione OPTIONS del file con estensione \] hpj. Questo comando è per la compatibilità con le versioni precedenti. Le nuove applicazioni devono fornire un file con estensione cnt e usare il comando HELP \_ FINDER.                                           | Ignorato; impostato su 0.                                                                                                                                                                                                                                                                                           |
| CONTESTO \_ DELLA GUIDA       | Visualizza l'argomento identificato dall'identificatore di contesto specificato definito nella \[ sezione MAP del file con estensione \] hpj.                                                                                                                                                   | Contiene l'identificatore di contesto per l'argomento.                                                                                                                                                                                                                                                               |
| HELP \_ CONTEXTMENU   | Visualizza **il** menu ? per la finestra selezionata, quindi visualizza l'argomento per il controllo selezionato in una finestra popup.                                                                                                                                             | Indirizzo di una matrice di **coppie DWORD.** Il primo **valore DWORD** in ogni coppia è l'identificatore del controllo e il secondo è l'identificatore di contesto per l'argomento. La matrice deve terminare con una coppia di zeri {0,0} . Se non si vuole aggiungere la Guida a un determinato controllo, impostarne l'identificatore di contesto su -1. |
| CONTESTO \_ DELLA GUIDAPOPUP  | Visualizza l'argomento identificato dall'identificatore di contesto specificato definito nella sezione MAP del \[ \] file hpj in una finestra popup.                                                                                                                                | Contiene l'identificatore di contesto per un argomento.                                                                                                                                                                                                                                                                 |
| RICERCA DELLA \_ GUIDA        | Consente di visualizzare **la finestra di dialogo** Argomenti della Guida.                                                                                                                                                                                                                             | Ignorato; impostato su 0.                                                                                                                                                                                                                                                                                           |
| HELP \_ FORCEFILE     | Garantisce che Windows help visualizza il file della Guida corretto. Se viene visualizzato il file della Guida non corretto, Windows guida apre quello corretto. In caso contrario, non viene eseguita alcuna azione.                                                                                     | Ignorato; impostato su 0.                                                                                                                                                                                                                                                                                           |
| HELP \_ HELPONHELP    | Visualizza la Guida su come usare Windows, se è disponibile il file Winhlp32.hlp.                                                                                                                                                                                     | Ignorato; impostato su 0.                                                                                                                                                                                                                                                                                           |
| INDICE \_ DELLA GUIDA         | Visualizza l'argomento specificato dall'opzione Contenuto nella \[ sezione OPTIONS del file con estensione \] hpj. Questo comando è per la compatibilità con le versioni precedenti. Le nuove applicazioni devono usare il comando HELP \_ FINDER.                                                                   | Ignorato; impostato su 0.                                                                                                                                                                                                                                                                                           |
| CHIAVE \_ DELLA GUIDA           | Visualizza l'argomento nella tabella delle parole chiave che corrisponde alla parola chiave specificata, se esiste una corrispondenza esatta. Se è presente più di una corrispondenza, visualizza l'indice con gli argomenti elencati nella **casella di riepilogo** Argomenti trovati .                                                 | Indirizzo di una stringa di parola chiave. Più parole chiave devono essere separate da punti e virgola.                                                                                                                                                                                                                              |
| HELP \_ MULTIKEY      | Visualizza l'argomento specificato da una parola chiave in una tabella di parole chiave alternativa.                                                                                                                                                                                           | Indirizzo di una [**struttura MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) che specifica un carattere di nota a piè di pagina e una parola chiave della tabella.                                                                                                                                                                                     |
| HELP \_ PARTIALKEY    | Visualizza l'argomento nella tabella delle parole chiave che corrisponde alla parola chiave specificata, se esiste una corrispondenza esatta. Se è presente più di una corrispondenza, viene visualizzata la **finestra di dialogo** Argomenti trovati . Per visualizzare l'indice senza passare una parola chiave, usare un puntatore a una stringa vuota. | Indirizzo di una stringa di parola chiave. Più parole chiave devono essere separate da punti e virgola.                                                                                                                                                                                                                              |
| HELP \_ QUIT          | Informa Windows guida che non è più necessaria. Se nessun'altra applicazione ha richiesto assistenza, Windows chiude Windows Guida.                                                                                                                                         | Ignorato; impostato su 0.                                                                                                                                                                                                                                                                                           |
| HELP \_ SETCONTENTS   | Specifica l'argomento Contents. Windows Guida visualizza questo argomento quando l'utente fa clic sul **pulsante Contenuto** se al file della Guida non è associato un file con estensione cnt.                                                                                                  | Contiene l'identificatore di contesto per l'argomento Contents.                                                                                                                                                                                                                                                      |
| HELP \_ SETPOPUP \_ POS | Imposta la posizione della finestra popup successiva.                                                                                                                                                                                                                   | Contiene i dati relativi alla posizione. Usare la macro [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) per concatenare le coordinate orizzontale e verticale in un singolo valore. La finestra popup viene posizionata come se il cursore del mouse si trovava nel punto specificato quando è stata richiamata la finestra popup.                                 |
| HELP \_ SETWINPOS     | Visualizza la Windows guida, se è ridotta a icona o in memoria, e ne imposta le dimensioni e la posizione come specificato.                                                                                                                                                      | Indirizzo di una [**struttura HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) che specifica le dimensioni e la posizione di una finestra della Guida primaria o secondaria.                                                                                                                                                             |
| HELP \_ TCARD         | Indica che un comando è per un'istanza della scheda di training Windows Guida. Combinare questo comando con altri comandi usando l'operatore OR bit per bit.                                                                                                                    | Dipende dal comando con cui viene combinato questo comando.                                                                                                                                                                                                                                                  |
| GUIDA \_ DI WM \_      | Visualizza l'argomento per il controllo identificato dal *parametro hWndMain* in una finestra popup.                                                                                                                                                                        | Indirizzo di una matrice di **coppie DWORD.** Il primo **valore DWORD** in ogni coppia è un identificatore di controllo e il secondo è un identificatore di contesto per un argomento. La matrice deve terminare con una coppia di zeri {0,0} . Se non si vuole aggiungere la Guida a un determinato controllo, impostarne l'identificatore di contesto su -1.       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5.0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **MLWinHelpW** (Unicode) e **MLWinHelpA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
