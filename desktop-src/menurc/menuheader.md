---
title: Struttura MENUHEADER
description: Contiene informazioni sulla versione per la risorsa di menu. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Menu struttura MENUHEADER e altre risorse
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301025"
---
# <a name="menuheader-structure"></a>Struttura MENUHEADER

Contiene informazioni sulla versione per la risorsa di menu. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**wVersion**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di versione del modello di menu. Questo membro deve essere uguale a zero per indicare che si tratta di [**un \_ menu RT**](/windows/desktop/menurc/resource-types) creato con un modello di menu standard.

</dd> <dt>

**cbHeaderSize**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Dimensioni dell'intestazione del modello di menu. Questo valore è zero per i menu creati con un modello di menu standard.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_intestazione del modello menuex \_**](menuex-template-header.md)
</dt> <dt>

[**\_elemento del modello menuex \_**](menuex-template-item.md)
</dt> <dt>

[**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

