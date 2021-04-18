---
title: Struttura un'STRINGTABLE
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene informazioni sulla formattazione della lingua e della tabella codici per le stringhe specificate dal membro figlio. Una tabella codici è un set di caratteri ordinato.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menu struttura un'STRINGTABLE e altre risorse
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400365"
---
# <a name="stringtable-structure"></a>Struttura un'STRINGTABLE

Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene informazioni sulla formattazione della lingua e della tabella codici per le stringhe specificate dal membro **figlio** . Una tabella codici è un set di caratteri ordinato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a>Members

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Lunghezza, in byte, della struttura **un'STRINGTABLE** , incluse tutte le strutture indicate dal membro **figlio** .

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

Numero esadecimale a 8 cifre archiviato come stringa Unicode. Le quattro cifre più significative rappresentano l'identificatore della lingua. Le quattro cifre meno significative rappresentano la tabella codici per la quale vengono formattati i dati. Ogni identificatore di linguaggio standard Microsoft contiene due parti: i 10 bit di ordine inferiore specificano la lingua principale e i 6 bit più significativi specificano il linguaggio di sottolinguaggio. Per una tabella di identificatori validi, vedere.

</dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Il numero di parole necessarie per allineare il membro **figlio** al limite di 32 bit è pari a zero.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **stringa**](string-str.md)**

</dd> <dd>

Matrice di una o più strutture di [**stringa**](string-str.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).

Il membro **figlio** della struttura [**StringFileInfo**](stringfileinfo.md) contiene almeno una struttura **un'STRINGTABLE** .

Impostare la parte relativa alla tabella codici del membro **szKey** sul valore esadecimale 0x04B0 per indicare la tabella codici Unicode o sul valore esadecimale della tabella codici appropriata per il componente del linguaggio. Dopo aver scelto il valore per la tabella codici, è necessario continuare a usare lo stesso valore nelle revisioni successive del file.

Un file eseguibile o una DLL che supporta più lingue deve avere una risorsa di versione per ogni lingua, anziché una singola risorsa di versione contenente stringhe in diverse lingue. Tuttavia, se si usa la struttura [**var**](var-str.md) per elencare le lingue supportate dall'applicazione, il numero di strutture **un'STRINGTABLE** nella risorsa Version è direttamente correlato al numero di coppie lingua/identificatore tabella codici nel membro **value** della struttura **var** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Stringa**](string-str.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sulla versione](version-information.md)
</dt> </dl>

 

 





