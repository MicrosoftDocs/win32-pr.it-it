---
description: Inviato da un'estensione di file Manager per fare in modo che file Manager ridisegni la finestra attiva o tutte le finestre.
title: Messaggio FM_REFRESH_WINDOWS (Wfext. h)
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
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225800"
---
# <a name="fm_refresh_windows-message"></a>\_Messaggio di \_ Windows Refresh Refresh

Inviato da un'estensione di file Manager per fare in modo che file Manager ridisegni la finestra attiva o tutte le finestre.

## <a name="parameters"></a>Parametri

<dl> <dt>

*fRepaint* 
</dt> <dd>

Valore che indica se Gestione file ridisegna la finestra attiva o tutte le finestre. Se questo parametro è **true**, gestione file ridisegna tutte le relative finestre. In caso contrario, file Manager ridisegna solo la finestra attiva.

</dd> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le modifiche del file System provocate da un'estensione vengono rilevate automaticamente da file Manager. Un'estensione deve utilizzare questo messaggio solo nelle situazioni in cui le connessioni alle unità vengono effettuate o annullate.

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

 

 




