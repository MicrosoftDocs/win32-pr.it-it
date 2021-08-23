---
title: SB_GETTIPTEXT messaggio (Commctrl.h)
description: Recupera il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere creata con lo stile SBT \_ TOOLTIPS per abilitare le descrizioni comando.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT del messaggio Windows controlli
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a78fa6650d850cad2b6de8cc77f1d44b49b8325bf6856b989953fc6511f56f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637131"
---
# <a name="sb_gettiptext-message"></a>Messaggio \_ GETTIPTEXT SB

Recupera il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere creata con lo stile [**SBT \_ TOOLTIPS**](status-bar-styles.md) per abilitare le descrizioni comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

LoWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) l'indice in base zero della parte che riceve il testo della descrizione comando. La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica le dimensioni del buffer in *corrispondenza di lParam,* in caratteri.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer di caratteri che riceve il testo della descrizione comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso errato di questo messaggio può causare problemi per l'applicazione. Ad esempio, se il testo è troppo grande per il buffer *lParam,* potrebbe causare un overflow del buffer. Prima di [continuare, è consigliabile](sec-comctls.md) esaminare Considerazioni sulla sicurezza: Controlli Windows Microsoft.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ GETTIPTEXTW** (Unicode) e **SB \_ GETTIPTEXTA** (ANSI)<br/>               |



 

