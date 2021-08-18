---
title: Struttura FONTGROUPHDR
description: Contiene le informazioni necessarie per un'applicazione per accedere a un tipo di carattere specifico. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Struttura FONTGROUPHDR Menu e altre risorse
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51b307b7f5798a57e344096fe46227edf97babbf3547c4c851d71fd8ecdc28da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734479"
---
# <a name="fontgrouphdr-structure"></a>Struttura FONTGROUPHDR

Contiene le informazioni necessarie per un'applicazione per accedere a un tipo di carattere specifico. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a>Members

<dl> <dt>

**NumberOfFonts**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Numero di singoli tipi di carattere associati a questa risorsa.

</dd> <dt>

**De**
</dt> <dd>

Tipo: **[ **DIRENTRY**](direntry.md)**

</dd> <dd>

Struttura che contiene un identificatore ordinale univoco per ogni tipo di carattere nella risorsa. Il **membro DE** è un segnaposto per la matrice a lunghezza variabile di strutture [**DIRENTRY.**](direntry.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura FONTGROUPHDR** segue i dati per i singoli tipi di carattere in . File Res. Il compilatore di risorse aggiunge automaticamente la **struttura FONTGROUPHDR,** in genere come ultima voce nel file.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DIRENTRY**](direntry.md)
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

 





