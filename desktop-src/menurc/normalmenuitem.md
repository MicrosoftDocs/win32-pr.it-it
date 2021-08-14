---
title: Struttura NORMALMENUITEM
description: Contiene informazioni su ogni voce di una risorsa di menu che non apre un menu o un sottomenu. La definizione della struttura qui fornita è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Struttura NORMALMENUITEM Menu e altre risorse
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f47fef5e1481d56671cd525061f1a5fcf88481213671bac45c923cfbae0ebbd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733691"
---
# <a name="normalmenuitem-structure"></a>Struttura NORMALMENUITEM

Contiene informazioni su ogni voce di una risorsa di menu che non apre un menu o un sottomenu. La definizione della struttura qui fornita è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a>Members

<dl> <dt>

**Resinfo**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo di voce di menu. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                       | Significato                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ END**</dt> <dt>0x80</dt> </dl>       | La voce di menu è l'ultima in questo sottomenu o in questa risorsa di menu. questo flag viene usato internamente dal sistema.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ POPUP**</dt> <dt>0x01</dt> </dl> | La voce di menu apre un menu o un sottomenu. il flag viene usato internamente dal sistema. <br/>                    |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Stringa Unicode con terminazione Null che contiene il testo per questa voce di menu. Non esiste alcun limite fisso per le dimensioni di questa stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Esiste una struttura **NORMALMENUITEM** per ogni voce di menu che non apre un menu o un sottomenu. Indicare l'ultima voce di menu in un menu impostando il membro **resInfo** su **MFR \_ END**.

Un separatore di menu è un tipo speciale di voce di menu inattiva ma visualizzata come barra di divisione tra due voci di menu attive. Indicare un separatore di menu lasciando vuoto **il membro menuText.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

 





