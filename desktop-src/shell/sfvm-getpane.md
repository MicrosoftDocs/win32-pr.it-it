---
description: SFVM \_ GetPane può essere modificato o non disponibile.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Messaggio SFVM_GETPANE (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967838"
---
# <a name="sfvm_getpane-message"></a>\_Messaggio GETPANE SFVM

\[**SFVM \_ GetPane** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Consente all'oggetto callback di fornire il riquadro della barra di stato in cui visualizzare le informazioni sull'area Internet. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*paneID* \[ in\]
</dt> <dd>

ID del riquadro richiesto. Si tratta in genere \_ di una zona del riquadro, ma può essere uno dei valori seguenti.

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span id="PANE_NONE"></span><span id="pane_none"></span>**\_nessun riquadro**


</dt> <dd>

Nessun riquadro.

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>**area del riquadro \_**


</dt> <dd>

Riquadro dell'area Internet.

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**RIQUADRO \_ offline**


</dt> <dd>

Il riquadro offline.

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>**stampante riquadri \_**


</dt> <dd>

Riquadro dell'indicazione di stampa.

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>**SSL del riquadro \_**


</dt> <dd>

Il riquadro SSL.

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**\_navigazione riquadro**


</dt> <dd>

Riquadro di spostamento.

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**\_stato riquadro**


</dt> <dd>

Riquadro indicatore di stato.

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PRIVACY del riquadro \_**


</dt> <dd>

Riquadro dell'indicatore della privacy.

</dd> </dl> </dd> <dt>

*riquadro* \[ out\]
</dt> <dd>

Puntatore a un **valore DWORD** contenente il numero del riquadro.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                                                      |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
