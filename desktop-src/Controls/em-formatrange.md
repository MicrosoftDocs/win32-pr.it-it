---
title: EM_FORMATRANGE messaggio (Richedit.h)
description: Formatta un intervallo di testo in un controllo Rich Edit per un dispositivo specifico.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE di controllo Windows messaggio
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
ms.openlocfilehash: 941aceb8c8f91657c7f78aba3d83a627fc413ed20d71217c933c6fba9b6f39e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049351"
---
# <a name="em_formatrange-message"></a>Messaggio \_ EM FORMATRANGE

Formatta un intervallo di testo in un controllo Rich Edit per un dispositivo specifico.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se eseguire il rendering del testo. Se questo parametro è diverso da zero, viene eseguito il rendering del testo. In caso contrario, il testo viene misurato.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) contenente informazioni sul dispositivo di output o **NULL** per liberare informazioni memorizzate nella cache dal controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce l'indice dell'ultimo carattere che rientra nell'area, più 1.

## <a name="remarks"></a>Commenti

Questo messaggio viene in genere usato per formattare il contenuto del controllo Rich Edit per un dispositivo di output, ad esempio una stampante.

Dopo aver utilizzato questo messaggio per formattare un intervallo di testo, è importante liberare le informazioni memorizzate nella cache inviando nuovamente **EM \_ FORMATRANGE,** ma con *lParam* impostato su **NULL.** In caso contrario, si verificherà una perdita di memoria. Inoltre, dopo aver utilizzato questo messaggio per un dispositivo, è necessario liberare le informazioni memorizzate nella cache prima di usarle di nuovo per un dispositivo diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ DISPLAYBAND**](em-displayband.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Stampa di controlli Rich Edit](printing-rich-edit-controls.md)
</dt> </dl>

 

 





