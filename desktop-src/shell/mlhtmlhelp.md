---
description: Visualizza una finestra della guida che corrisponde all'impostazione della lingua dell'interfaccia utente corrente.
title: MLHtmlHelp (funzione)
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
ms.openlocfilehash: a477ef549b3b8437ba891259c7fecea4730f759e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993800"
---
# <a name="mlhtmlhelp-function"></a>MLHtmlHelp (funzione)

\[Questa funzione è disponibile tramite Windows XP e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Visualizza una finestra della guida che corrisponde all'impostazione della lingua dell'interfaccia utente corrente.

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

*hwndCaller* \[ in\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra padre che chiama questa funzione.

</dd> <dt>

*pszFile* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a un buffer che contiene il percorso completo di un file della Guida compilato (con estensione chm) o un file di argomento all'interno di un file della Guida specificato.

</dd> <dt>

*uCommand* \[ in\]
</dt> <dd>

Tipo: **uint**

Comando da completare. Questa funzione supporta direttamente solo [l' \_ \_ argomento di visualizzazione HH](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) e il [ \_ \_ \_ popup del testo visualizzato HH](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command). Nel caso di qualsiasi altro comando, la chiamata viene trasmessa senza il valore di *dwCrossCodePage* a [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).

</dd> <dt>

*dwData* \[ in\]
</dt> <dd>

Tipo: **DWORD \_ ptr**

Tutti i dati che potrebbero essere necessari, in base al valore del parametro *uCommand* .

</dd> <dt>

*dwCrossCodePage* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Valore **DWORD** che indica la tabella codici dell'impostazione della lingua dell'interfaccia utente corrente, ad esempio CP \_ ACP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HWND**

A seconda del *uCommand* specificato e del risultato, **MLHtmlHelp** restituisce uno o entrambi gli elementi seguenti:

-   Handle (HWND) della finestra della guida.
-   **Valore null**. In alcuni casi, **null** indica un errore. in altri casi, **null** indica che la finestra della guida non è stata ancora creata.

## <a name="remarks"></a>Commenti

Se si verifica un problema con il percorso del file della Guida per la lingua corrente, la chiamata viene trasmessa a [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) per la gestione standard.

Quando la finestra della guida è chiusa, lo stato attivo torna al proprietario, a meno che il proprietario non sia il desktop. Se *hwndCaller* è il desktop, il sistema operativo determina la posizione in cui viene restituito lo stato attivo.

Inoltre, se **MLHtmlHelp** invia messaggi di notifica dalla finestra della guida, i messaggi vengono inviati a *hwndCaller* , purché sia stata abilitata la verifica dei [messaggi di notifica](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) nella definizione della finestra della guida.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene chiamato il comando [HH \_ display \_ Topic](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) per aprire il file della Guida denominato Help. chm e visualizzare il relativo argomento predefinito nella finestra della guida denominata `Mainwin` . In genere, la finestra della Guida specificata in questo comando è un [Visualizzatore della Guida HTML](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)standard.

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> Quando si usa questa funzione, impostare la dimensione dello stack del file eseguibile di hosting su almeno 100.000. Se la dimensione dello stack definita è troppo piccola, il thread creato per eseguire la Guida HTML verrà creato anche con questa dimensione dello stack e l'operazione potrebbe non riuscire. Facoltativamente, è possibile rimuovere/STACK dalla riga di comando del collegamento e rimuovere anche eventuali impostazioni dello STACK nel file DEF dell'eseguibile. in questo caso, la dimensione predefinita dello stack è 1 MB. È anche possibile impostare le dimensioni dello stack usando il comando del compilatore/fnumber (il compilatore lo passerà al linker come/STACK).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **MLHtmlHelpW** (Unicode) e **MLHtmlHelpA** (ANSI)<br/>                                               |



 

 
