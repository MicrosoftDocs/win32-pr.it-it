---
description: Inviato a una procedura DLL di estensione di file Manager quando l'utente preme F1 su un elemento del comando del menu o della barra degli strumenti. L'estensione deve chiamare WinHelp, con il parametro HWND della funzione impostato sul valore del parametro HWND dell'estensione.
title: Messaggio FMEVENT_HELPMENUITEM (Wfext. h)
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
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977090"
---
# <a name="fmevent_helpmenuitem-message"></a>\_Messaggio FMEVENT HELPMENUITEM

Inviato a una procedura DLL di estensione di file Manager quando l'utente preme F1 su un elemento del comando del menu o della barra degli strumenti. L'estensione deve chiamare [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), con il parametro *HWND* della funzione impostato sul valore del parametro *HWND* dell'estensione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*uItem* 
</dt> <dd>

Valore che identifica l'elemento di comando del menu o della barra degli strumenti per il quale si desidera la guida. La procedura di estensione usa questo valore per determinare il modo migliore per chiamare [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una procedura DLL di estensione deve restituire zero se elabora questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**\_HELPSTRING FMEVENT**](fmevent-helpstring.md)
</dt> </dl>

 

 




