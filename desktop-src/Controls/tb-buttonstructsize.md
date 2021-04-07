---
title: Messaggio TB_BUTTONSTRUCTSIZE (COMmctrl. h)
description: Specifica la dimensione della struttura TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- Controlli di Windows Message TB_BUTTONSTRUCTSIZE
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
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048771"
---
# <a name="tb_buttonstructsize-message"></a>TB \_ BUTTONSTRUCTSIZE messaggio

Specifica la dimensione della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione, in byte, della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il sistema utilizza la dimensione per determinare quale versione della libreria di collegamento dinamico (DLL) del controllo comune viene utilizzata.

Se un'applicazione usa la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare la barra degli strumenti, l'applicazione deve inviare questo messaggio alla barra degli strumenti prima di inviare il messaggio [**TB \_ ADDBITMAP**](tb-addbitmap.md) o [**TB \_ ADDBUTTONS**](tb-addbuttons.md) . La funzione [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) invia automaticamente **TB \_ BUTTONSTRUCTSIZE** e le dimensioni della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) sono un parametro della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

