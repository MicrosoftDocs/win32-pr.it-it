---
title: Struttura StringTable
description: Rappresenta l'organizzazione dei dati in una risorsa con versione file. Contiene informazioni sulla lingua e sulla formattazione della tabella codici per le stringhe specificate dal membro Children. Una tabella codici è un set di caratteri ordinato.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menu della struttura StringTable e altre risorse
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01ad7a2436c4b32f0f2fa09ab801339903ed55f35be80bbfc43c4542da4e4ce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720661"
---
# <a name="stringtable-structure"></a>Struttura StringTable

Rappresenta l'organizzazione dei dati in una risorsa con versione file. Contiene informazioni sulla lingua e sulla formattazione della tabella codici per le stringhe specificate dal **membro Children.** Una tabella codici è un set di caratteri ordinato.

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

Tipo: **WORD**

</dd> <dd>

Lunghezza, in byte, di **questa struttura StringTable,** incluse tutte le strutture indicate dal **membro Children.**

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Questo membro è sempre uguale a zero.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo di dati nella risorsa della versione. Questo membro è 1 se la risorsa versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Numero esadecimale a 8 cifre archiviato come stringa Unicode. Le quattro cifre più significative rappresentano l'identificatore della lingua. Le quattro cifre meno significative rappresentano la tabella codici per cui vengono formattati i dati. Ogni identificatore della lingua standard Microsoft contiene due parti: i 10 bit meno importanti specificano la lingua principale e i 6 bit di ordine elevato specificano il sottolinguaggio. Per una tabella di identificatori validi, vedere .

</dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tutte le parole zero necessarie per allineare il **membro Children** su un limite a 32 bit.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **Stringa**](string-str.md)**

</dd> <dd>

Matrice di una o più [**strutture String.**](string-str.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in nessuno dei file di intestazione forniti con Windows Software Development Kit (SDK).

Il **membro Children** della struttura [**StringFileInfo**](stringfileinfo.md) contiene almeno una **struttura StringTable.**

Impostare la parte della tabella codici del membro **szKey** sul valore esadecimale 0x04b0 per indicare la tabella codici Unicode o sul valore esadecimale della tabella codici appropriato per il componente di linguaggio. Dopo aver scelto il valore per la tabella codici, è consigliabile continuare a usare lo stesso valore nelle revisioni successive del file.

Un file eseguibile o una DLL che supporta più lingue deve avere una risorsa di versione per ogni lingua, anziché una singola risorsa di versione che contiene stringhe in più lingue. Tuttavia, se si usa la struttura [**Var**](var-str.md) per elencare i linguaggi supportati dall'applicazione, il numero di strutture **StringTable** nella risorsa versione è direttamente correlato al numero di coppie di identificatori di linguaggio/tabella codici nel membro **Value** della struttura **Var.**

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

 

 





