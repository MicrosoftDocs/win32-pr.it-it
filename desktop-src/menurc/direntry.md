---
title: Struttura DIRENTRY
description: Contiene un ordinale univoco che identifica un singolo tipo di carattere nel gruppo di risorse del tipo di carattere. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Struttura DIRENTRY Menu e altre risorse
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 281ede8b2f87e73bf0600d985abd3194a83e8e8f186fa8f780f18f80985e0f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602111"
---
# <a name="direntry-structure"></a>Struttura DIRENTRY

Contiene un ordinale univoco che identifica un singolo tipo di carattere nel gruppo di risorse del tipo di carattere. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**fontOrdinal**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Identificatore ordinale univoco per un singolo tipo di carattere in un gruppo di risorse del tipo di carattere.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [**struttura FONTDIRENTRY**](fontdirentry.md) per il tipo di carattere specificato segue direttamente la **struttura DIRENTRY** per tale tipo di carattere.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

 





