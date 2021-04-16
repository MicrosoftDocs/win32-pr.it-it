---
title: Messaggio SB_SETTIPTEXT (COMmctrl. h)
description: Imposta il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere stata creata con lo \_ stile SBT Tooltips per abilitare le descrizioni comandi.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- Controlli di Windows Message SB_SETTIPTEXT
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478095"
---
# <a name="sb_settiptext-message"></a>\_Messaggio SETTIPTEXT SB

Imposta il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere stata creata con lo stile [**SBT \_ Tooltips**](status-bar-styles.md) per abilitare le descrizioni comandi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della parte che riceverà il testo della descrizione comando.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer di caratteri che contiene il nuovo testo della descrizione comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

Questo testo della descrizione comando viene visualizzato in due situazioni:

-   Quando il riquadro corrispondente nella barra di stato contiene solo un'icona.
-   Quando il riquadro corrispondente nella barra di stato contiene testo troncato a causa delle dimensioni del riquadro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ SETTIPTEXTW** (Unicode) e **SB \_ SETTIPTEXTA** (ANSI)<br/>               |



 

 





