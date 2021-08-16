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
ms.openlocfilehash: fa38b55fdcd7c338102ed62bd9d7011ca4b7caf79fa81e834bcf915d8f934464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224267"
---
# <a name="fm_refresh_windows-message"></a>Messaggio \_ DI WINDOWS FM REFRESH \_

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

Le modifiche al file system causate da un'estensione vengono rilevate automaticamente da File Manager. Un'estensione deve usare questo messaggio solo in situazioni in cui le connessioni all'unità vengono effettuate o annullate.

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

 

 




