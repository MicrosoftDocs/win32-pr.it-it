---
title: MENUEX_TEMPLATE_HEADER struttura
description: Definisce l'intestazione per un modello di menu esteso. Questa definizione di struttura è solo a scopo di spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER struttura menu e altre risorse
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31e52661e04a036cf7a49791be96af002b801af0e0ed1c4b6ad3ddebf971c2c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226121"
---
# <a name="menuex_template_header-structure"></a>Struttura MENUEX \_ TEMPLATE \_ HEADER

Definisce l'intestazione per un modello di menu esteso. Questa definizione di struttura è solo a scopo di spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**wVersion**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Numero di versione del modello. Questo membro deve essere 1 per i modelli di menu estesi.

</dd> <dt>

**wOffset**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Offset della prima struttura [**MENUEX \_ TEMPLATE \_ ITEM,**](menuex-template-item.md) rispetto alla fine di questo membro della struttura. Se la definizione del primo elemento segue immediatamente **il membro dwHelpId,** questo membro deve essere 4.

</dd> <dt>

**dwHelpId**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificatore della Guida della barra dei menu.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un modello di menu esteso è costituito da **una struttura MENUEX \_ TEMPLATE \_ HEADER** seguita da una o più strutture [**MENUEX TEMPLATE \_ \_ ITEM**](menuex-template-item.md) contigue. Le **strutture MENUEX \_ TEMPLATE \_ ITEM,** di lunghezza variabile, sono allineate ai **limiti DWORD.** Per creare un menu da un modello di menu esteso in memoria, usare la [**funzione LoadMenuIndirect.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**VOCE DEL MODELLO \_ \_ MENUEX**](menuex-template-item.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

 





