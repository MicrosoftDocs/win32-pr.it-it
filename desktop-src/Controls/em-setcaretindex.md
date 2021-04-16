---
title: Messaggio EM_SETCARETINDEX (CommCtrl. h)
description: Imposta il valore di indice in base zero della posizione del cursore in un controllo di modifica.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Controlli di Windows Message EM_SETCARETINDEX
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478580"
---
# <a name="em_setcaretindex-message"></a>\_Messaggio SETCARETINDEX em

Imposta il valore di indice in base zero della posizione del cursore in un controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuovo valore di indice in base zero della posizione del cursore.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Se l'indice non è compreso nell'intervallo del testo in un controllo di modifica, l'indice verrà regolato in modo da adattarsi all'intervallo del testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10, 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETCARETINDEX em**](em-getcaretindex.md)
</dt> </dl>

 

 





