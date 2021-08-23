---
description: Ottiene un set di flag che indicano le opzioni correnti della visualizzazione.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: Proprietà ShellFolderView.ViewOptions (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3c49389700494c646976ee7df5e67782b110fc085f4328cb139b9604523c8622
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968430"
---
# <a name="shellfolderviewviewoptions-property"></a>ShellFolderView.ViewOptions - proprietà

Ottiene un set di flag che indicano le opzioni correnti della visualizzazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a>Valore proprietà

Variabile di tipo [**IDispatch che**](/windows/win32/api/oaidl/nn-oaidl-idispatch) riceve l'oggetto delle opzioni di visualizzazione. Contiene uno o più dei valori seguenti:

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO \_ SHOWALLOBJECTS** (0x00000001)


</dt> <dd>

**L'opzione Mostra tutti i** file è abilitata.

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO \_ SHOWEXTENSIONS** (0x00000002)


</dt> <dd>

**L'opzione Nascondi estensioni per i tipi di file** noti è disabilitata.

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO \_ SHOWCOMPCOLOR** (0x00000008)


</dt> <dd>

**L'opzione Visualizza file e cartelle compressi con colore** alternativo è abilitata.

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO \_ SHOWSYSFILES** (0x00000020)


</dt> <dd>

**L'opzione Non visualizzare file nascosti** è abilitata.

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO \_ WIN95CLASSIC** (0x00000040)


</dt> <dd>

**L'opzione Stile** classico è abilitata.

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO \_ DOUBLECLICKINWEBVIEW** (0x00000080)


</dt> <dd>

**L'opzione Doppio clic per aprire un elemento** è abilitata.

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO \_ DESKTOPHTML** (0x00000200)


</dt> <dd>

**L'opzione Active Desktop - Visualizza come pagina Web** è abilitata.

</dd> </dl>

## <a name="remarks"></a>Commenti

[**FocusedItem**](shellfolderview-focuseditem.md) può essere chiamato solo nel sistema locale. Non funzionerà quando viene eseguito in una pagina Web tramite HTTP o UNC.

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso corretto di questo metodo JScript incorporato in HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 
