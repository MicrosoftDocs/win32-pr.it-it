---
description: Inviato da un'estensione di file Manager (o un'altra applicazione) per fare in modo che file Manager ricarichi tutte le DLL di estensione elencate nella \[ \] sezione addons del file Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Messaggio FM_RELOAD_EXTENSIONS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979714"
---
# <a name="fm_reload_extensions-message"></a>\_Messaggio estensioni di RIcaricamento FM \_

Inviato da un'estensione di file Manager (o un'altra applicazione) per fare in modo che file Manager ricarichi tutte le DLL di estensione elencate nella \[ \] sezione addons del file Winfile.ini.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Altre applicazioni possono utilizzare la funzione [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) per inviare questo messaggio a gestione file. Per ottenere l'handle di finestra del file Manager appropriato, un'applicazione può specificare "WFS \_ frame" come parametro *lpszClassName* in una chiamata alla funzione [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
