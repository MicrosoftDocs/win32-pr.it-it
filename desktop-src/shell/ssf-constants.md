---
description: Usato dalla funzione SHGetSetSettings per specificare i membri della relativa struttura SHELLSTATE da impostare o recuperati.
title: Costanti SSF (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2a883110-fdc3-4451-9e47-e58894600e3b
api_name:
- SSF_SHOWALLOBJECTS
- SSF_SHOWEXTENSIONS
- SSF_HIDDENFILEEXTS
- SSF_SERVERADMINUI
- SSF_SHOWCOMPCOLOR
- SSF_SORTCOLUMNS
- SSF_SHOWSYSFILES
- SSF_DOUBLECLICKINWEBVIEW
- SSF_SHOWATTRIBCOL
- SSF_DESKTOPHTML
- SSF_WIN95CLASSIC
- SSF_DONTPRETTYPATH
- SSF_MAPNETDRVBUTTON
- SSF_SHOWINFOTIP
- SSF_HIDEICONS
- SSF_NOCONFIRMRECYCLE
- SSF_FILTER
- SSF_WEBVIEW
- SSF_SHOWSUPERHIDDEN
- SSF_SEPPROCESS
- SSF_NONETCRAWLING
- SSF_STARTPANELON
- SSF_SHOWSTARTPAGE
- SSF_AUTOCHECKSELECT
- SSF_ICONSONLY
- SSF_SHOWTYPEOVERLAY
- SSF_SHOWSTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b26ba102ff72caf235a51d3888183ccafba9d639
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994829"
---
# <a name="ssf-constants"></a>Costanti SSF

Usato dalla funzione [**SHGetSetSettings**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings) per specificare i membri della relativa struttura [**ShellState**](/windows/win32/api/shlobj_core/ns-shlobj_core-shellstatea) da impostare o recuperati.

<dl> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**\_SHOWALLOBJECTS SSF**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



È in corso la richiesta del membro **fShowAllObjects** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**\_SHOWEXTENSIONS SSF**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



È in corso la richiesta del membro **fShowExtensions** .


</dt> </dl> </dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**\_HIDDENFILEEXTS SSF**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Non usato.


</dt> </dl> </dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**\_SERVERADMINUI SSF**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Non usato.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**\_SHOWCOMPCOLOR SSF**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



È in corso la richiesta del membro **fShowCompColor** .


</dt> </dl> </dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**\_SORTCOLUMNS SSF**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Sono richiesti i membri **lParamSort** e **iSortDirection** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**\_SHOWSYSFILES SSF**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



È in corso la richiesta del membro **fShowSysFiles** .


</dt> </dl> </dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**\_DOUBLECLICKINWEBVIEW SSF**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



È in corso la richiesta del membro **fDoubleClickInWebView** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**\_SHOWATTRIBCOL SSF**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



È in corso la richiesta del membro **fShowAttribCol** .

**Windows Vista:** Non utilizzato.


</dt> </dl> </dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**\_DESKTOPHTML SSF**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



È in corso la richiesta del membro **fDesktopHTML** . Il set non è disponibile. Per le versioni di Windows precedenti a Windows XP, è invece possibile abilitare il codice HTML per desktop da [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop). L'utilizzo di **IActiveDesktop** a questo scopo, tuttavia, non è consigliato per Windows XP e versioni successive di Windows ed è deprecato in Windows Vista.


</dt> </dl> </dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**\_WIN95CLASSIC SSF**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



È in corso la richiesta del membro **fWin95Classic** .


</dt> </dl> </dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**\_DONTPRETTYPATH SSF**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



È in corso la richiesta del membro **fDontPrettyPath** .


</dt> </dl> </dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**\_MAPNETDRVBUTTON SSF**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



È in corso la richiesta del membro **fMapNetDrvBtn** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**\_SHOWINFOTIP SSF**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



È in corso la richiesta del membro **fShowInfoTip** .


</dt> </dl> </dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**\_HIDEICONS SSF**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



È in corso la richiesta del membro **fHideIcons** .


</dt> </dl> </dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**\_NOCONFIRMRECYCLE SSF**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



È in corso la richiesta del membro **fNoConfirmRecycle** .


</dt> </dl> </dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**\_filtro SSF**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



È in corso la richiesta del membro **fFilter** .

**Windows Vista:** Non utilizzato.


</dt> </dl> </dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**WebView SSF \_**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



È in corso la richiesta del membro **fWebView** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**\_SHOWSUPERHIDDEN SSF**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



È in corso la richiesta del membro **fShowSuperHidden** .


</dt> </dl> </dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**\_SEPPROCESS SSF**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



È in corso la richiesta del membro **fSepProcess** .


</dt> </dl> </dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**\_NONETCRAWLING SSF**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



**Windows XP e versioni successive**. È in corso la richiesta del membro **fNoNetCrawling** .


</dt> </dl> </dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**\_STARTPANELON SSF**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



**Windows XP e versioni successive**. È in corso la richiesta del membro **fStartPanelOn** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**\_SHOWSTARTPAGE SSF**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Non usato.


</dt> </dl> </dd> <dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**\_AUTOCHECKSELECT SSF**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



**Windows Vista e versioni successive**. È in corso la richiesta del membro **fAutoCheckSelect** .


</dt> </dl> </dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**\_ICONSONLY SSF**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



**Windows Vista e versioni successive**. È in corso la richiesta del membro **fIconsOnly** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**\_SHOWTYPEOVERLAY SSF**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



**Windows Vista e versioni successive**. È in corso la richiesta del membro **fShowTypeOverlay** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTATUSBAR"></span><span id="ssf_showstatusbar"></span>**\_SHOWSTATUSBAR SSF**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



**Windows 8 e versioni successive**: è richiesto il membro **fShowStatusBar** .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
