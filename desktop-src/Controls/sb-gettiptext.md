---
title: Messaggio SB_GETTIPTEXT (COMmctrl. h)
description: Recupera il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere creata con lo \_ stile della descrizione comando SBT per abilitare le descrizioni comandi.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- Controlli di Windows Message SB_GETTIPTEXT
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
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874229"
---
# <a name="sb_gettiptext-message"></a>\_Messaggio GETTIPTEXT SB

Recupera il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere creata con lo stile della [**\_ Descrizione comando SBT**](status-bar-styles.md) per abilitare le descrizioni comandi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica l'indice in base zero della parte che riceve il testo della descrizione comando. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la dimensione del buffer in corrispondenza di *lParam*, in caratteri.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer di caratteri che riceve il testo della descrizione comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso errato di questo messaggio può causare problemi per l'applicazione. Se, ad esempio, il testo è troppo grande per il buffer *lParam* , potrebbe verificarsi un overflow del buffer. Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ GETTIPTEXTW** (Unicode) e **SB \_ GETTIPTEXTA** (ANSI)<br/>               |



 

