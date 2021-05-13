---
description: Inviato a una procedura DLL di estensione di File Manager quando l'utente preme F1 su un menu o una voce di comando della barra degli strumenti. L'estensione deve chiamare WinHelp, con il parametro hwnd della funzione impostato sul valore del parametro hwnd dell'estensione.
title: FMEVENT_HELPMENUITEM messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: 46cb246e91f9901204432527ba36fd8ac72beba4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842312"
---
# <a name="fmevent_helpmenuitem-message"></a>Messaggio \_ HELPMENUITEM FMEVENT

Inviato a una procedura DLL di estensione di File Manager quando l'utente preme F1 su un menu o una voce di comando della barra degli strumenti. L'estensione deve [**chiamare WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), con il parametro *hwnd* della funzione impostato sul valore del parametro *hwnd* dell'estensione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*uItem* 
</dt> <dd>

Valore che identifica la voce di menu o di comando della barra degli strumenti per cui si desidera visualizzare la Guida. La procedura di estensione usa questo valore per determinare il modo migliore per chiamare [**WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una routine DLL di estensione deve restituire zero se elabora questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPSTRING**](fmevent-helpstring.md)
</dt> </dl>

 

 




