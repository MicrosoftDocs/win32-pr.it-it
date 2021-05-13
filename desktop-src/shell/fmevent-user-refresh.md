---
description: Inviato a una DLL di estensione quando l'utente sceglie il comando Aggiorna dal menu Visualizza in File Manager. L'estensione può usare questa notifica per aggiornare il relativo menu.
title: FMEVENT_USER_REFRESH messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: 16f75f562149b50237a6b41bf2023d1f694741e3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841262"
---
# <a name="fmevent_user_refresh-message"></a>MESSAGGIO DI \_ AGGIORNAMENTO \_ DELL'UTENTE FMEVENT

Inviato a una DLL di estensione quando l'utente sceglie il **comando Aggiorna** dal menu **Visualizza** in File Manager. L'estensione può usare questa notifica per aggiornare il relativo menu.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una DLL di estensione deve restituire zero se elabora questo messaggio.

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

 

 




