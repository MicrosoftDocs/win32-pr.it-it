---
description: Inviato da un'estensione di File Manager (o da un'altra applicazione) per fare in modo che File Manager ricarica tutte le DLL di estensione elencate nella sezione AddOns del \[ \] file Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: FM_RELOAD_EXTENSIONS messaggio (Wfext.h)
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
ms.openlocfilehash: 9e4e632ac153a78e729ce0d3fcd65f49ae90781bd29cfe354d4571ba04e63be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224175"
---
# <a name="fm_reload_extensions-message"></a>Messaggio FM \_ RELOAD \_ EXTENSIONS

Inviato da un'estensione di File Manager (o da un'altra applicazione) per fare in modo che File Manager ricarica tutte le DLL di estensione elencate nella sezione AddOns del \[ \] file Winfile.ini.

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

Altre applicazioni possono usare la [**funzione PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) per inviare questo messaggio a File Manager. Per ottenere l'handle di finestra di File Manager appropriato, un'applicazione può specificare "WFS Frame" come parametro \_ *lpszClassName* in una chiamata alla [**funzione FindWindow.**](/windows/win32/api/winuser/nf-winuser-findwindowa)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
