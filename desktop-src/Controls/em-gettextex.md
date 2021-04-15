---
title: Messaggio di EM_GETTEXTEX (RichEdit. h)
description: Ottiene il testo da un controllo Rich Edit.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- Controlli di Windows Message EM_GETTEXTEX
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476480"
---
# <a name="em_gettextex-message"></a>\_Messaggio GETTEXTEX em

Ottiene il testo da un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a una struttura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , che indica come tradurre il testo prima di inserirlo nel buffer di output.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer per ricevere il testo. Le dimensioni del buffer, in byte, sono specificate dal membro **CB** della struttura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) . Usare il [**messaggio \_ GetTextLengthEx em**](em-gettextlengthex.md) per ottenere la dimensione richiesta del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di **TCHAR** copiate nel buffer di output, incluso il carattere di terminazione null.

## <a name="remarks"></a>Commenti

Se la dimensione del buffer di output è inferiore alla dimensione del testo nel controllo, il controllo di modifica copia il testo dall'inizio e lo inserisce nel buffer finché il buffer non è pieno. Un carattere di terminazione null verrà ancora inserito alla fine del buffer.

Se viene richiesto testo ANSI, **em \_ GETTEXTEX** usa la funzione [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) per convertire i caratteri Unicode in ANSI. Consente di passare da Unicode a ANSI usando una determinata tabella codici. La struttura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) contiene i membri (**lpDefaultChar** e **lpUsedDefChar**) usati nella conversione da Unicode ad ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_SETTEXTEX em**](em-settextex.md)
</dt> <dt>

[**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[**\_testo WM**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

