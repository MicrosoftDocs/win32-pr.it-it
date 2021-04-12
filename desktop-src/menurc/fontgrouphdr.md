---
title: Struttura FONTGROUPHDR
description: Contiene le informazioni necessarie a un'applicazione per accedere a un tipo di carattere specifico. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Menu struttura FONTGROUPHDR e altre risorse
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225228"
---
# <a name="fontgrouphdr-structure"></a>Struttura FONTGROUPHDR

Contiene le informazioni necessarie a un'applicazione per accedere a un tipo di carattere specifico. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

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

Tipo: **Word**

</dd> <dd>

Numero di singoli tipi di carattere associati a questa risorsa.

</dd> <dt>

**DE**
</dt> <dd>

Tipo: **[ **dirente**](direntry.md)**

</dd> <dd>

Struttura che contiene un identificatore ordinale univoco per ogni tipo di carattere nella risorsa. Il membro **de** è un segnaposto per la matrice a lunghezza variabile delle strutture di [**dislocazione**](direntry.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **FONTGROUPHDR** segue i dati per i singoli tipi di carattere in. File res. Il compilatore di risorse aggiunge automaticamente la struttura **FONTGROUPHDR** , in genere come ultima voce nel file.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Diaffitto**](direntry.md)
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

 





