---
title: TB_BUTTONSTRUCTSIZE messaggio (Commctrl.h)
description: Specifica le dimensioni della struttura TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- TB_BUTTONSTRUCTSIZE del messaggio Windows controlli
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceed10eec9038b338d060f28acdab8a10aa88aecef6b264b6d6d0682168f4937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919141"
---
# <a name="tb_buttonstructsize-message"></a>TB \_ BUTTONSTRUCTSIZE message

Specifica le dimensioni della struttura [**TBBUTTON.**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione, in byte, della [**struttura TBBUTTON.**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il sistema usa le dimensioni per determinare la versione della libreria di collegamento dinamico (DLL) di controllo comune in uso.

Se un'applicazione usa la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare la barra degli strumenti, l'applicazione deve inviare questo messaggio alla barra degli strumenti prima di inviare il messaggio [**\_ TB ADDBITMAP**](tb-addbitmap.md) o [**TB \_ ADDBUTTONS.**](tb-addbuttons.md) La [**funzione CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) invia automaticamente **TB \_ BUTTONSTRUCTSIZE** e le dimensioni della [**struttura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) sono un parametro della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

