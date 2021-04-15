---
title: Messaggio di EM_SETTEXTEX (RichEdit. h)
description: Combina la funzionalità dei messaggi WM \_ REPLACESEL e em e \_ consente di impostare il testo usando una tabella codici e di usare testo RTF o testo normale.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- Controlli di Windows Message EM_SETTEXTEX
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477309"
---
# <a name="em_settextex-message"></a>\_Messaggio SETTEXTEX em

Combina la funzionalità dei messaggi [**WM \_**](/windows/desktop/winmsg/wm-settext) [**\_ REPLACESEL e em**](em-replacesel.md) e consente di impostare il testo usando una tabella codici e di usare testo RTF o testo normale.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a una struttura [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) che specifica i flag e una tabella codici facoltativa da usare per la conversione in Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al testo con terminazione null da inserire. Questo testo è una stringa ANSI, a meno che la tabella codici non sia 1200 (Unicode). Se *lParam* inizia con una sequenza ASCII RTF valida, ad esempio "{ \\ RTF" o "{urtf", il testo viene letto usando il lettore RTF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione sta impostando tutto il testo e ha esito positivo, il valore restituito è 1.

Se l'operazione sta impostando la selezione e ha esito positivo, il valore restituito è il numero di byte o caratteri copiati.

Se l'operazione ha esito negativo, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETTEXTEX em**](em-gettextex.md)
</dt> <dt>

[**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

