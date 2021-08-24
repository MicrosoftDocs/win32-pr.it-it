---
title: SB_SETTIPTEXT messaggio (Commctrl.h)
description: Imposta il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere stata creata con lo stile SBT \_ TOOLTIPS per abilitare le descrizioni comando.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- SB_SETTIPTEXT dei controlli Windows messaggio
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
ms.openlocfilehash: 864ba53066b000f9f7ae65365341238a701b4e70bc4ce8cc70adba923d57a5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637021"
---
# <a name="sb_settiptext-message"></a>Messaggio \_ SETTIPTEXT SB

Imposta il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere stata creata con lo [**stile SBT \_ TOOLTIPS**](status-bar-styles.md) per abilitare le descrizioni comando.

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ SETTIPTEXTW** (Unicode) e **SB \_ SETTIPTEXTA** (ANSI)<br/>               |



 

 





