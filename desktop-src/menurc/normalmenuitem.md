---
title: Struttura NORMALMENUITEM
description: Contiene informazioni su ogni elemento in una risorsa di menu che non apre un menu o un sottomenu. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Menu struttura NORMALMENUITEM e altre risorse
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340513"
---
# <a name="normalmenuitem-structure"></a>Struttura NORMALMENUITEM

Contiene informazioni su ogni elemento in una risorsa di menu che non apre un menu o un sottomenu. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a>Members

<dl> <dt>

**resInfo**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tipo di voce di menu. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                       | Significato                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**Fabbisogno \_ di FINE**</dt> <dt>0x80</dt> </dl>       | La voce di menu è l'ultima in questo sottomenu o risorsa di menu; Questo flag viene utilizzato internamente dal sistema.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**Fabbisogno \_ di POPUP**</dt> <dt>0x01</dt> </dl> | La voce di menu apre un menu o un sottomenu; il flag viene utilizzato internamente dal sistema. <br/>                    |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Stringa Unicode con terminazione null che contiene il testo di questa voce di menu. Non esiste un limite fisso per le dimensioni di questa stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Esiste una struttura **NORMALMENUITEM** per ogni voce di menu che non apre un menu o un sottomenu. Indica l'ultima voce di menu in un menu impostando il membro **resInfo** su **fabbisogno \_ finale**.

Un separatore di menu è un tipo speciale di voce di menu che è inattivo, ma viene visualizzato come una barra di divisione tra due voci di menu attive. Indicare un separatore di menu lasciando vuoto il membro **menuText** .

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

 

 





