---
title: Struttura RESOURCEHEADER
description: Contiene informazioni sull'intestazione della risorsa stessa e sui dati specifici di questa risorsa.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Struttura RESOURCEHEADER Menu e altre risorse
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78b1c6468f251ac48340baf584234f22e325b392798afad436643aa0792e8369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687101"
---
# <a name="resourceheader-structure"></a>Struttura RESOURCEHEADER

Contiene informazioni sull'intestazione della risorsa stessa e sui dati specifici di questa risorsa. Questa struttura non è una vera struttura in linguaggio C, perché contiene membri a lunghezza variabile. La definizione della struttura fornita qui è solo a solo supporto della spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**DataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensione, in byte, dei dati che seguono l'intestazione della risorsa per questa particolare risorsa. Non include il riempimento dei file tra questa risorsa e le risorse che la seguono nel file di risorse.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni, in byte, dei dati dell'intestazione della risorsa che seguono.

</dd> <dt>

**TYPE**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo di risorsa. Il **membro TYPE** può essere un valore numerico o una stringa Unicode con terminazione Null che specifica il nome del tipo. Per una descrizione dei membri di tipo **Name** o **Ordinal,** vedere la sezione Osservazioni seguente.

Se il **membro TYPE** è un valore numerico, può specificare un tipo di risorsa standard o definito dall'utente. Se il membro è una stringa, è un tipo di risorsa definito dall'utente. Per un elenco dei tipi di risorse predefiniti, vedere [Tipi di risorse.](/windows/desktop/menurc/resource-types)

I valori minori di 256 sono riservati per l'uso da parte del sistema.

</dd> <dt>

**NOME**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Nome che identifica la risorsa specifica. Il **membro NAME,** come il **membro TYPE,** può essere un valore numerico o una stringa Unicode con terminazione Null. Per una descrizione dei membri di tipo **Name** o **Ordinal,** vedere la sezione Osservazioni seguente.

Non è necessario aggiungere spaziatura interna per **l'allineamento DWORD** tra i membri **TYPE** e **NAME** perché contengono **dati WORD.** Tuttavia, potrebbe essere necessario aggiungere una **parola** di riempimento dopo il membro **NAME** per allineare il resto dell'intestazione **sui limiti DWORD.**

</dd> <dt>

**DataVersion**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Versione dei dati delle risorse predefinita. Ciò determinerà la versione dei dati delle risorse che l'applicazione deve usare.

</dd> <dt>

**MemoryFlags**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Set di flag di attributi che possono descrivere lo stato della risorsa. Modificatori in . Il file di script RC assegna questi attributi alla risorsa. Gli identificatori di script possono assegnare i valori di flag seguenti.

Le applicazioni non usano nessuno di questi attributi. Gli attributi sono consentiti nello script per garantire la compatibilità con gli script esistenti, ma vengono ignorati. Le risorse vengono caricate quando viene caricato il modulo corrispondente e vengono liberate quando il modulo viene scaricato.

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

**MOVEABLE** (0x0010)


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

**FIXED** (~MOVEABLE)


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

**PURE** (0x0020)


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

**IMPURE** (~PURE)


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

**PRELOAD** (0x0040)


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

**LOADONCALL** (~PRELOAD)


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

**DISCARDABLE** (0x1000)


</dt> <dd></dd> </dl> </dd> <dt>

**Languageid**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Lingua per la risorsa o il set di risorse. Impostare il valore per questo membro con l'istruzione facoltativa di definizione della risorsa [LANGUAGE.](./language-statement.md) I parametri sono costanti del file Winnt.h.

Ogni risorsa include un identificatore di lingua in modo che il sistema o l'applicazione possa selezionare una lingua appropriata per le impostazioni locali correnti del sistema. Se sono presenti più risorse dello stesso tipo e nome che differiscono solo per la lingua delle stringhe all'interno delle risorse, sarà necessario specificare un **LanguageId** per ognuna.

</dd> <dt>

**Version**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero di versione definito dall'utente per i dati delle risorse che gli strumenti possono usare per leggere e scrivere i file di risorse. Impostare questo valore con l'istruzione [facoltativa VERSION](./version-statement.md) per la definizione della risorsa.

</dd> <dt>

**Caratteristiche**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Specifica informazioni definite dall'utente sulla risorsa che gli strumenti possono usare per leggere e scrivere file di risorse. Impostare questo valore con l'istruzione facoltativa di definizione della risorsa [CHARACTERISTICS.](./characteristics-statement.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Un membro di tipo variabile è denominato **membro Name** o **Ordinal** e viene usato nella maggior parte dei punti del file di risorse in cui viene visualizzato un identificatore. La prima **parola** di un **membro di** tipo Name o **Ordinal** indica se il membro è un valore numerico o una stringa. Se la prima **parola** nel membro è uguale al valore 0xffff, che è un carattere Unicode non valido, la parola **seguente** è un numero di tipo. In caso contrario, il membro contiene una stringa Unicode e la **prima parola** nel membro è il primo carattere nella stringa del nome. Per altre informazioni sulle istruzioni di definizione delle risorse, vedere [Istruzioni di definizione delle risorse.](./resource-definition-statements.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Istruzione CHARACTERISTICS](./characteristics-statement.md)
</dt> <dt>

[Istruzione LANGUAGE](./language-statement.md)
</dt> <dt>

[Istruzione VERSION](./version-statement.md)
</dt> </dl>

 

