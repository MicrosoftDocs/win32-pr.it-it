---
description: Inviato da un'estensione di File Manager per recuperare le informazioni sull'unità dalla finestra di Gestione file attiva.
title: FM_GETDRIVEINFO messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 39df15a4522e863fada40d3c964d709f40d2a26d01240aaefe51b09924b8c9ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459121"
---
# <a name="fm_getdriveinfo-message"></a>Messaggio \_ FM GETDRIVEINFO

Inviato da un'estensione di File Manager per recuperare le informazioni sull'unità dalla finestra di Gestione file attiva.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

Indirizzo di una [**struttura \_ GETDRIVEINFO FMS**](fms-getdriveinfo.md) che riceve informazioni sull'unità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero.

## <a name="remarks"></a>Commenti

Se 0xFFFFFFFF viene restituito nel membro **dwTotalSpace** o **dwFreeSpace** della struttura [**\_ FMS GETDRIVEINFO,**](fms-getdriveinfo.md) la libreria di estensioni deve calcolare il valore o i valori.

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

 

 




