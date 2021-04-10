---
title: Messaggio EM_ENABLESEARCHWEB (CommCtrl. h)
description: Abilita o Disabilita la funzionalità "Cerca sul Web" e la voce del menu di scelta rapida.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Controlli di Windows Message EM_ENABLESEARCHWEB
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964478"
---
# <a name="em_enablesearchweb-message"></a>\_Messaggio ENABLESEARCHWEB em

Abilita o Disabilita la funzionalità "Cerca sul Web" e la voce del menu di scelta rapida.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Il valore **true** indica che è abilitata la funzionalità "Cerca sul Web" e il valore **false** indica che è disabilitato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Se si disattiva "Cerca sul Web" utilizzando questo messaggio, il [**messaggio \_ SEARCHWEB em**](em-searchweb.md) non ha alcun effetto.

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

[**\_SEARCHWEB em**](em-searchweb.md)
</dt> </dl>

 

 





