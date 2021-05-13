---
description: Specifica una funzione di callback definita dall'applicazione chiamata da File Manager per comunicare con un'estensione di File Manager.
title: Funzione di callback FMExtensionProc (Wfext.h)
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
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842242"
---
# <a name="fmextensionproc-callback-function"></a>Funzione di callback FMExtensionProc

Specifica una funzione di callback definita dall'applicazione chiamata da File Manager per comunicare con un'estensione di File Manager.

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

*Hwnd* 
</dt> <dd>

Tipo: **HWND**

Handle di finestra per File Manager. Un'estensione usa questo handle per specificare la finestra padre per qualsiasi finestra di dialogo o finestra di messaggio che deve visualizzare e per inviare messaggi di query a File Manager.

</dd> <dt>

*wMsg* 
</dt> <dd>

Tipo: **WORD**

Uno dei messaggi di File Manager seguenti.

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**Da 1 a 99**


</dt> <dd>

L'utente ha selezionato una voce dal menu fornito dall'estensione. Il valore è l'identificatore della voce di menu selezionata.

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**


</dt> <dd>

L'utente ha premuto F1 durante la selezione di un menu di estensione o di un elemento di comando della barra degli strumenti. Indica che l'estensione deve chiamare **WinHelp** in modo appropriato per l'elemento di comando.

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**


</dt> <dd>

L'utente ha selezionato un menu di estensione o una voce di comando della barra degli strumenti. Indica che l'estensione deve fornire una stringa della Guida.

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**


</dt> <dd>

L'utente ha selezionato il menu dell'estensione. L'estensione deve inizializzare le voci nel menu.

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ LOAD**


</dt> <dd>

Gestione file carica la DLL di estensione e richiede informazioni sul menu fornito dalla DLL.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**


</dt> <dd>

La selezione nella **finestra directory di File Manager** o nella finestra **Risultati** ricerca è stata modificata.

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**


</dt> <dd>

Gestione file crea la barra degli strumenti e richiede alla DLL di estensione informazioni su eventuali pulsanti aggiunti dalla DLL alla barra degli strumenti.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**


</dt> <dd>

Gestione file sta scaricando la DLL dell'estensione.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT \_ USER \_ REFRESH**


</dt> <dd>

L'utente **ha selezionato** il comando Aggiorna dal menu Finestra.  Se necessario, l'estensione deve aggiornare le voci del menu.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Tipo: **LONG**

Valore specifico del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LONG**

Restituisce un valore dipendente dal messaggio *del parametro wMsg.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **FMExtensionProcW** (Unicode)<br/>                                          |



 

 




