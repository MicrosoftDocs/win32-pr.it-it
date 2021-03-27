---
description: Inviato da un'estensione di file Manager per recuperare il numero di file selezionati nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca). Il conteggio include i file con nomi di file lunghi.
title: Messaggio FM_GETSELCOUNTLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994757"
---
# <a name="fm_getselcountlfn-message"></a>\_Messaggio GETSELCOUNTLFN FM

Inviato da un'estensione di file Manager per recuperare il numero di file selezionati nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca). Il conteggio include i file con nomi di file lunghi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di file selezionati.

## <a name="remarks"></a>Commenti

Questo messaggio deve essere utilizzato solo dalle estensioni che supportano nomi di file lunghi (ad esempio, le estensioni che supportano la rete).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETFILESEL FM**](fm-getfilesel.md)
</dt> <dt>

[**\_GETFILESELLFN FM**](fm-getfilesellfn.md)
</dt> <dt>

[**\_GETSELCOUNT FM**](fm-getselcount.md)
</dt> </dl>

 

 




