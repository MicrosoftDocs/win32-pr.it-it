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
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842412"
---
# <a name="fm_getdriveinfo-message"></a>Messaggio \_ FM GETDRIVEINFO

Inviato da un'estensione di File Manager per recuperare le informazioni sull'unità dalla finestra di Gestione file attiva.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

Indirizzo di una [**struttura FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) che riceve le informazioni sull'unità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero.

## <a name="remarks"></a>Commenti

Se 0xFFFFFFFF viene restituito nel membro **dwTotalSpace** o **dwFreeSpace** della struttura [**FMS \_ GETDRIVEINFO,**](fms-getdriveinfo.md) la libreria di estensioni deve calcolare il valore o i valori.

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

 

 




