---
title: Struttura StringFileInfo
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene informazioni sulla versione che possono essere visualizzate per una lingua e una tabella codici particolari.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Menu struttura StringFileInfo e altre risorse
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963893"
---
# <a name="stringfileinfo-structure"></a>Struttura StringFileInfo

Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene informazioni sulla versione che possono essere visualizzate per una lingua e una tabella codici particolari.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a>Members

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Lunghezza, in byte, dell'intero blocco **StringFileInfo** , incluse tutte le strutture indicate dal membro **figlio** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Questo membro è sempre uguale a zero.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tipo di dati nella risorsa della versione. Questo membro è 1 se la risorsa della versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Stringa Unicode L "StringFileInfo".

</dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Il numero di parole necessarie per allineare il membro **figlio** al limite di 32 bit è pari a zero.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **un'STRINGTABLE**](stringtable.md)**

</dd> <dd>

Matrice di una o più strutture [**un'STRINGTABLE**](stringtable.md) . Ogni membro **szKey** della struttura **un'STRINGTABLE** indica la lingua e la tabella codici appropriate per la visualizzazione del testo nella struttura **un'STRINGTABLE** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).

Il membro **figlio** della struttura di [**Visual Studio \_ VERSIONINFO**](vs-versioninfo.md) può contenere zero o più strutture **StringFileInfo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Un'STRINGTABLE**](stringtable.md)
</dt> <dt>

[**Stringa**](string-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sulla versione](version-information.md)
</dt> </dl>

 

 





