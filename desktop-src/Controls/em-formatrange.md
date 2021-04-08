---
title: Messaggio di EM_FORMATRANGE (RichEdit. h)
description: Formatta un intervallo di testo in un controllo Rich Edit per un dispositivo specifico.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- Controlli di Windows Message EM_FORMATRANGE
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873941"
---
# <a name="em_formatrange-message"></a>\_Messaggio FormatRange em

Formatta un intervallo di testo in un controllo Rich Edit per un dispositivo specifico.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se eseguire il rendering del testo. Se questo parametro è diverso da zero, viene eseguito il rendering del testo. In caso contrario, il testo viene semplicemente misurato.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) contenente informazioni sul dispositivo di output oppure **null** per liberare informazioni memorizzate nella cache dal controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce l'indice dell'ultimo carattere che rientra nell'area, più 1.

## <a name="remarks"></a>Commenti

Questo messaggio viene in genere usato per formattare il contenuto del controllo Rich Edit per un dispositivo di output, ad esempio una stampante.

Dopo aver usato questo messaggio per formattare un intervallo di testo, è importante liberare le informazioni memorizzate nella cache inviando nuovamente **em \_ FormatRange** , ma con *lParam* impostato su **null**. in caso contrario, si verificherà una perdita di memoria. Inoltre, dopo aver usato questo messaggio per un dispositivo, è necessario liberare le informazioni memorizzate nella cache prima di riutilizzarlo per un dispositivo diverso.

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

[**\_DISPLAYBAND em**](em-displayband.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Stampa di controlli Rich Edit](printing-rich-edit-controls.md)
</dt> </dl>

 

 





