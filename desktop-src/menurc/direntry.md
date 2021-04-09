---
title: Struttura di diaffitto
description: Contiene un ordinale univoco che identifica un singolo tipo di carattere nel gruppo di risorse del tipo di carattere. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menu della struttura di dirente e altre risorse
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742031"
---
# <a name="direntry-structure"></a>Struttura di diaffitto

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

Tipo: **Word**

</dd> <dd>

Identificatore ordinale univoco per un singolo tipo di carattere in un gruppo di risorse dei tipi di carattere.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura [**FONTDIRENTRY**](fontdirentry.md) per il tipo di carattere specificato segue direttamente la struttura di **dislocazione** per tale tipo di carattere.

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

 

 





