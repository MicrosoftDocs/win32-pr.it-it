---
description: SFVM \_ GETPANE può essere modificato o non disponibile.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: SFVM_GETPANE messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef936d4218c29c8d0574e97b8de73c1a0d54f4d62df7dba4f43f371bfeaf95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968670"
---
# <a name="sfvm_getpane-message"></a>Messaggio \_ SFVM GETPANE

\[**SFVM \_ GETPANE** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Consente all'oggetto callback di fornire il riquadro della barra di stato in cui visualizzare le informazioni sull'area Internet. Usato da [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*paneID* \[ Pollici\]
</dt> <dd>

ID del riquadro richiesto. Si tratta in genere di PANE \_ ZONE, ma può essere uno dei valori seguenti.

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span id="PANE_NONE"></span><span id="pane_none"></span>**RIQUADRO \_ NESSUNO**


</dt> <dd>

Nessun riquadro.

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>**ZONA \_ DEL RIQUADRO**


</dt> <dd>

Riquadro Area Internet.

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**RIQUADRO \_ OFFLINE**


</dt> <dd>

Riquadro offline.

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>**STAMPANTE \_ RIQUADRO**


</dt> <dd>

Riquadro delle indicazioni di stampa.

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>**SSL DEL \_ RIQUADRO**


</dt> <dd>

Riquadro SSL.

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**NAVIGAZIONE NEL \_ RIQUADRO**


</dt> <dd>

Riquadro di spostamento.

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**STATO DEL \_ RIQUADRO**


</dt> <dd>

Riquadro dell'indicatore di stato.

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PRIVACY DEL \_ RIQUADRO**


</dt> <dd>

Riquadro dell'indicatore di privacy.

</dd> </dl> </dd> <dt>

*riquadro* \[ Cambio\]
</dt> <dd>

Puntatore a un **valore DWORD** contenente il numero del riquadro.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                                                      |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
