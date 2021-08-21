---
title: TTM_DELTOOL messaggio (Commctrl.h)
description: Rimuove uno strumento da un controllo descrizione comando.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- TTM_DELTOOL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea54eefd2b9cc84b3aabe5dd600c5fcc32c7468cae01d1819b5fda7b631aeabd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166384"
---
# <a name="ttm_deltool-message"></a>TTM \_ DELTOOL message

Rimuove uno strumento da un controllo descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) I **membri hwnd** **e uId** identificano lo strumento da rimuovere e il membro **cbSize** deve specificare le dimensioni della struttura. Tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ DELTOOLW** (Unicode) e **TTM \_ DELTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TTM \_ ADDTOOL**](ttm-addtool.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui controlli descrizione comando](tooltip-controls.md)
</dt> </dl>

 

 





