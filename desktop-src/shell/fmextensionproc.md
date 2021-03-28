---
description: Specifica una funzione di callback definita dall'applicazione chiamata da file Manager per comunicare con un'estensione di file Manager.
title: Funzione di callback FMExtensionProc (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 40e18dfe64c6d2b24b982cdf891cbb63b091a7ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993688"
---
# <a name="fmextensionproc-callback-function"></a>Funzione di callback FMExtensionProc

Specifica una funzione di callback definita dall'applicazione chiamata da file Manager per comunicare con un'estensione di file Manager.

## <a name="syntax"></a>Sintassi


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Tipo: **HWND**

Handle di finestra per file Manager. Un'estensione utilizza questo handle per specificare la finestra padre per qualsiasi finestra di dialogo o finestra di messaggio che deve visualizzare e per inviare messaggi di query a gestione file.

</dd> <dt>

*wMsg* 
</dt> <dd>

Tipo: **Word**

Uno dei seguenti messaggi di gestione file.

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**da 1 a 99**


</dt> <dd>

L'utente ha selezionato un elemento dal menu fornito dall'estensione. Il valore è l'identificatore della voce di menu selezionata.

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**\_HELPMENUITEM FMEVENT**


</dt> <dd>

Premere F1 durante la selezione di un menu di estensione o di un elemento del comando della barra degli strumenti. Indica che l'estensione deve chiamare **WinHelp** in modo appropriato per l'elemento di comando.

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**\_HELPSTRING FMEVENT**


</dt> <dd>

L'utente ha selezionato un menu di estensione o un elemento comando della barra degli strumenti. Indica che l'estensione deve fornire una stringa della guida.

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**\_INITMENU FMEVENT**


</dt> <dd>

L'utente ha selezionato il menu dell'estensione. L'estensione deve inizializzare gli elementi nel menu.

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**\_carico FMEVENT**


</dt> <dd>

Gestione file sta caricando la DLL di estensione e richiede la DLL per informazioni sul menu fornito dalla DLL.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**\_selChange FMEVENT**


</dt> <dd>

La selezione nella finestra Directory di **file Manager** o nella finestra **Risultati ricerca** è stata modificata.

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**\_TOOLBARLOAD FMEVENT**


</dt> <dd>

La barra degli strumenti viene creata da Gestione file e viene richiesta la DLL di estensione per informazioni sui pulsanti aggiunti dalla DLL alla barra degli strumenti.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**\_scaricamento FMEVENT**


</dt> <dd>

Il file Manager sta scaricando la DLL di estensione.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**\_aggiornamento utente \_ FMEVENT**


</dt> <dd>

L'utente ha selezionato il comando **Aggiorna** dal menu **finestra** . Se necessario, l'estensione deve aggiornare gli elementi nel menu.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Tipo: **Long**

Valore specifico del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **Long**

Restituisce un valore che dipende dal messaggio di parametro *wmsg* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **FMExtensionProcW** (Unicode)<br/>                                          |



 

 




