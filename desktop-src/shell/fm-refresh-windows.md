---
description: Inviato da un'estensione di File Manager per fare in modo che File Manager ridisegni la finestra attiva o tutte le finestre.
title: FM_REFRESH_WINDOWS messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 0513955fd1b03dfae321d52fe9a5df3794f54782
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842352"
---
# <a name="fm_refresh_windows-message"></a>MESSAGGIO \_ DI WINDOWS FM REFRESH \_

Inviato da un'estensione di File Manager per fare in modo che File Manager ridisegni la finestra attiva o tutte le finestre.

## <a name="parameters"></a>Parametri

<dl> <dt>

*fRepaint* 
</dt> <dd>

Valore che indica se File Manager ridisegna la finestra attiva o tutte le finestre. Se questo parametro è **TRUE,** File Manager ridisegna tutte le finestre. In caso contrario, File Manager ridisegna solo la finestra attiva.

</dd> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le modifiche al file system causate da un'estensione vengono rilevate automaticamente da File Manager. Un'estensione deve utilizzare questo messaggio solo nelle situazioni in cui le connessioni alle unità vengono effettuate o annullate.

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

 

 




