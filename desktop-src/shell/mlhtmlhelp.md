---
description: Visualizza una finestra della Guida che corrisponde all'impostazione corrente della lingua dell'interfaccia utente.
title: Funzione MLHtmlHelp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: c38e84df2ca6f379e7d479125f1f454a10426406ba40ad21721fe01f67cce6f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090211"
---
# <a name="mlhtmlhelp-function"></a>Funzione MLHtmlHelp

\[Questa funzione è disponibile tramite Windows XP e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Visualizza una finestra della Guida che corrisponde all'impostazione corrente della lingua dell'interfaccia utente.

## <a name="syntax"></a>Sintassi


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndCaller* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra padre che chiama questa funzione.

</dd> <dt>

*pszFile* \[ Pollici\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a un buffer che contiene il percorso completo di un file della Guida compilato (con estensione chm) o di un file di argomento all'interno di un file della Guida specificato.

</dd> <dt>

*uCommand* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Comando da completare. Questa funzione supporta direttamente solo [HH \_ DISPLAY TOPIC \_ e](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) [HH DISPLAY TEXT \_ \_ \_ POPUP.](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command) Nel caso di qualsiasi altro comando, la chiamata viene inoltrata senza il *valore dwCrossCodePage* a [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).

</dd> <dt>

*dwData* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD \_ PTR**

Tutti i dati che possono essere necessari, in base al valore del *parametro uCommand.*

</dd> <dt>

*dwCrossCodePage* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Valore **DWORD** che indica la tabella codici dell'impostazione corrente della lingua dell'interfaccia utente, ad esempio CP \_ ACP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HWND**

A seconda *dell'uCommand specificato* e del risultato, **MLHtmlHelp** restituisce uno o entrambi gli elementi seguenti:

-   Handle (hwnd) della finestra della Guida.
-   **NULL**. In alcuni casi, **NULL** indica un errore. in altri **casi, NULL** indica che la finestra della Guida non è ancora stata creata.

## <a name="remarks"></a>Commenti

Se si verifica un problema con il percorso del file della Guida per la lingua corrente, la chiamata viene inoltrata [a HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) per la gestione standard.

Quando la finestra della Guida viene chiusa, lo stato attivo torna al proprietario, a meno che il proprietario non sia il desktop. Se *hwndCaller è* il desktop, il sistema operativo determina dove viene restituito lo stato attivo.

Inoltre, se **MLHtmlHelp** invia messaggi di notifica dalla finestra della Guida, i messaggi vengono [](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) inviati a *hwndCaller* purché sia stato abilitato il rilevamento dei messaggi di notifica nella definizione della finestra della Guida.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene chiamato il comando [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) per aprire il file della Guida denominato Help.chm e visualizzarne l'argomento predefinito nella finestra della Guida denominata `Mainwin` . In genere, la finestra della Guida specificata in questo comando è un [visualizzatore della Guida HTML standard.](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> Quando si usa questa funzione, impostare le dimensioni dello stack del file eseguibile di hosting su almeno 100.000. Se le dimensioni dello stack definite sono troppo piccole, anche il thread creato per eseguire la Guida HTML verrà creato con queste dimensioni dello stack e l'operazione potrebbe non riuscire. Facoltativamente, è possibile rimuovere /STACK dalla riga di comando del collegamento e anche rimuovere qualsiasi impostazione STACK nel file DEF del file eseguibile (in questo caso la dimensione predefinita dello stack è 1 MB). È anche possibile impostare le dimensioni dello stack usando il comando del compilatore /Fnumber (il compilatore lo passerà al linker come /STACK).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5.0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **MLHtmlHelpW** (Unicode) e **MLHtmlHelpA** (ANSI)<br/>                                               |



 

 
