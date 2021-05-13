---
description: Inviato a una DLL di estensione quando l'utente seleziona il menu per l'estensione dalla barra dei menu di File Manager. L'estensione può usare questa notifica per inizializzare le voci di menu.
title: FMEVENT_INITMENU messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 82ec9130a681bdfd36ff6259392c0608e4cde9cf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842282"
---
# <a name="fmevent_initmenu-message"></a>Messaggio \_ FMEVENT INITMENU

Inviato a una DLL di estensione quando l'utente seleziona il menu per l'estensione dalla barra dei menu di File Manager. L'estensione può usare questa notifica per inizializzare le voci di menu.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*Hmenu* 
</dt> <dd>

Handle per la barra dei menu di File Manager.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una DLL di estensione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Una DLL di estensione riceve questo messaggio solo quando l'utente seleziona il menu di primo livello. Se l'estensione contiene sottomenu, deve inizializzarli nello stesso momento in cui inizializza il menu di primo livello.

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

 

 




