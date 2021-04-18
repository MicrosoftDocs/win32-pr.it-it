---
title: Struttura RESOURCEHEADER
description: Contiene informazioni sull'intestazione della risorsa stessa e i dati specifici per questa risorsa.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Menu struttura RESOURCEHEADER e altre risorse
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301194"
---
# <a name="resourceheader-structure"></a>Struttura RESOURCEHEADER

Contiene informazioni sull'intestazione della risorsa stessa e i dati specifici per questa risorsa. Questa struttura non è una vera struttura del linguaggio C, perché contiene membri a lunghezza variabile. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

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

Dimensioni, in byte, dei dati che seguono l'intestazione della risorsa per la risorsa specifica. Non include alcun riempimento di file tra questa risorsa e tutte le risorse che lo seguono nel file di risorse.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensione, in byte, dei dati dell'intestazione della risorsa che seguono.

</dd> <dt>

**TYPE**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo di risorsa. Il membro del **tipo** può essere un valore numerico o una stringa Unicode con terminazione null che specifica il nome del tipo. Per una descrizione dei membri di tipo **nome** o **ordinale** , vedere la sezione Osservazioni riportata di seguito.

Se il membro del **tipo** è un valore numerico, può specificare un tipo di risorsa standard o definito dall'utente. Se il membro è una stringa, si tratta di un tipo di risorsa definito dall'utente. Per un elenco dei tipi di risorsa predefiniti, vedere [tipi di risorse](/windows/desktop/menurc/resource-types).

I valori minori di 256 sono riservati per l'utilizzo da parte del sistema.

</dd> <dt>

**NOME**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Nome che identifica la risorsa specifica. Il membro del **nome** , ad esempio il membro del **tipo** , può essere un valore numerico o una stringa Unicode con terminazione null. Per una descrizione dei membri di tipo **nome** o **ordinale** , vedere la sezione Osservazioni riportata di seguito.

Non è necessario aggiungere la spaziatura interna per l'allineamento **DWORD** tra i membri del **tipo** e del **nome** perché contengono dati di **Word** . Tuttavia, potrebbe essere necessario aggiungere una **parola** di riempimento dopo il membro del **nome** per allineare il resto dell'intestazione ai limiti **DWORD** .

</dd> <dt>

**Dataversion**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Versione di dati della risorsa predefinita. In questo modo verrà determinata la versione dei dati della risorsa che l'applicazione deve utilizzare.

</dd> <dt>

**MemoryFlags**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Set di flag di attributo che possono descrivere lo stato della risorsa. Modificatori in. Il file di script RC assegna questi attributi alla risorsa. Gli identificatori di script possono assegnare i valori dei flag seguenti.

Le applicazioni non utilizzano uno di questi attributi. Gli attributi sono consentiti nello script per la compatibilità con le versioni precedenti degli script esistenti, ma vengono ignorati. Le risorse vengono caricate quando viene caricato il modulo corrispondente e vengono liberate quando il modulo viene scaricato.

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

**Mobile** (0x0010)


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

**corretto** (~ mobile)


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

**Pure** (0x0020)


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

**impure** (~ pure)


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

**Precaricamento** (0x0040)


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

**LOADONCALL** (~ preload)


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

Annullabile **(0x1000** )


</dt> <dd></dd> </dl> </dd> <dt>

**LanguageId**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Lingua della risorsa o del set di risorse. Impostare il valore di questo membro con l'istruzione di definizione della risorsa della [lingua](./language-statement.md) facoltativa. I parametri sono costanti dal file Winnt. h.

Ogni risorsa include un identificatore di lingua, in modo che il sistema o l'applicazione possa selezionare una lingua appropriata per le impostazioni locali correnti del sistema. Se sono presenti più risorse dello stesso tipo e del nome che differiscono solo per la lingua delle stringhe all'interno delle risorse, è necessario specificare un **LanguageID** per ciascuna di esse.

</dd> <dt>

**Versione**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero di versione definito dall'utente per i dati della risorsa che gli strumenti possono usare per leggere e scrivere i file di risorse. Impostare questo valore con l'istruzione facoltativa della definizione della risorsa della [versione](./version-statement.md) .

</dd> <dt>

**Caratteristiche**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Specifica le informazioni definite dall'utente sulla risorsa che gli strumenti possono usare per leggere e scrivere i file di risorse. Impostare questo valore con l'istruzione di definizione di risorsa delle [caratteristiche](./characteristics-statement.md) facoltative.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un membro del tipo di variabile è denominato membro di **nome** o **ordinale** e viene usato nella maggior parte delle posizioni nel file di risorse in cui viene visualizzato un identificatore. La prima **parola** di un membro di tipo **nome** o **ordinale** indica se il membro è un valore numerico o una stringa. Se la prima **parola** nel membro è uguale al valore 0xFFFF, che è un carattere Unicode non valido, la **parola** seguente è un numero di tipo. In caso contrario, il membro contiene una stringa Unicode e la prima **parola** nel membro è il primo carattere nella stringa del nome. Per ulteriori informazioni sulle istruzioni di definizione di risorsa, vedere [istruzioni di definizione di risorse](./resource-definition-statements.md).

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

[Caratteristiche (istruzione)](./characteristics-statement.md)
</dt> <dt>

[LANGUAGE (istruzione)](./language-statement.md)
</dt> <dt>

[Istruzione VERSION](./version-statement.md)
</dt> </dl>

 

