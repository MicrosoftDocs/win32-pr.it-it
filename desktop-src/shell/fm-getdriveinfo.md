---
description: Inviato da un'estensione di file Manager per recuperare le informazioni sull'unità dalla finestra di gestione file attiva.
title: Messaggio FM_GETDRIVEINFO (Wfext. h)
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
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993704"
---
# <a name="fm_getdriveinfo-message"></a>\_Messaggio GETDRIVEINFO FM

Inviato da un'estensione di file Manager per recuperare le informazioni sull'unità dalla finestra di gestione file attiva.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

Indirizzo di una struttura [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) che riceve informazioni sull'unità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero.

## <a name="remarks"></a>Commenti

Se 0xFFFFFFFF viene restituito nel membro **dwTotalSpace** o **DwFreeSpace** della struttura [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) , la libreria di estensioni deve calcolare il valore o i valori.

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

 

 




