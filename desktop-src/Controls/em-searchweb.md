---
title: EM_SEARCHWEB messaggio (Commctrl.h)
description: Apre il browser ed esegue una ricerca Web con il testo selezionato come termine di ricerca.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SEARCHWEB di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21523df67acf91b8a44f59ea40b012f1af7c287185b7ac64b5dc1288005dfb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673177"
---
# <a name="em_searchweb-message"></a>MESSAGGIO \_ EM SEARCHWEB

Apre il browser ed esegue una ricerca Web con il testo selezionato come termine di ricerca.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Se la funzionalità "Cerca sul Web" è disabilitata usando il messaggio [**EM \_ ENABLESEARCHWEB,**](em-enablesearchweb.md) questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop 1809 \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2019 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> </dl>

 

 





