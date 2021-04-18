---
title: Struttura MENUEX_TEMPLATE_HEADER
description: Definisce l'intestazione per un modello di menu esteso. Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- Menu struttura MENUEX_TEMPLATE_HEADER e altre risorse
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301201"
---
# <a name="menuex_template_header-structure"></a>Struttura di intestazione del \_ modello menuex \_

Definisce l'intestazione per un modello di menu esteso. Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard.

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

Tipo: **Word**

</dd> <dd>

Numero di versione del modello. Questo membro deve essere 1 per i modelli di menu estesi.

</dd> <dt>

**wOffset**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Offset alla prima struttura dell' [**\_ \_ elemento del modello menuex**](menuex-template-item.md) , relativa alla fine del membro della struttura. Se la definizione del primo elemento segue immediatamente il membro **dwHelpId** , questo membro deve essere 4.

</dd> <dt>

**dwHelpId**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificatore della guida della barra dei menu.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un modello di menu esteso è costituito da una struttura di **\_ \_ intestazione del modello menuex** seguita da una o più strutture di [**\_ \_ elementi del modello menuex**](menuex-template-item.md) contigue. Le strutture degli **\_ \_ elementi del modello menuex** , che sono di lunghezza variabile, sono allineate ai limiti **DWORD** . Per creare un menu da un modello di menu esteso in memoria, usare la funzione [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .

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

[**\_elemento del modello menuex \_**](menuex-template-item.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

 





