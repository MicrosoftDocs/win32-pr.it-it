---
description: Inviato a una DLL di estensione quando File Manager scarica la DLL.
title: FMEVENT_UNLOAD messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 24b5b2a77393178cad545cb63c1524a8d7e92c5c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843072"
---
# <a name="fmevent_unload-message"></a>Messaggio FMEVENT \_ UNLOAD

Inviato a una DLL di estensione quando File Manager scarica la DLL.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una DLL di estensione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

I *valori hwnd* e **hMenu** passati con i messaggi [**FMEVENT \_ LOAD**](fmevent-load.md) e [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) potrebbero non essere validi al momento dell'invio del messaggio.

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

 

 




