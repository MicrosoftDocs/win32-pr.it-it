---
title: Risorsa User-Defined
description: Un'istruzione di definizione delle risorse definita dall'utente definisce una risorsa che contiene dati specifici dell'applicazione.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- risorsa definita dall'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221364"
---
# <a name="user-defined-resource"></a>Risorsa User-Defined

Un'istruzione di definizione delle risorse definita dall'utente definisce una risorsa che contiene dati specifici dell'applicazione. I dati possono avere qualsiasi formato e possono essere definiti come contenuto di un determinato file (se il parametro *filename* viene specificato) o come una serie di numeri e stringhe (se il blocco di *dati non elaborati* è specificato).

``` syntax
nameID typeID filename
```

*Filename* specifica il nome di un file contenente i dati binari della risorsa. Il contenuto del file è incluso come risorsa. RC non interpreta i dati binari in alcun modo. È responsabilità del programmatore garantire che i dati siano allineati correttamente per l'architettura del computer di destinazione.

È anche possibile definire completamente una risorsa definita dall'utente nello script della risorsa usando la sintassi seguente:

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome univoco o Unsigned Integer a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*
</dt> <dd>

Nome univoco o Unsigned Integer a 16 bit che identifica il tipo di risorsa. Se viene specificato un numero, il valore deve essere maggiore di 255. I numeri da 1 a 255 sono riservati ai tipi di risorse ridefiniti esistenti e futuri.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Nome del file che contiene i dati della risorsa. Il parametro deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente.

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*dati non elaborati*
</dt> <dd>

Dati non elaborati costituiti da uno o più numeri interi o stringhe di caratteri. I numeri interi possono essere specificati in formato decimale, ottale o esadecimale. Per essere compatibile con Windows a 16 bit, i numeri interi vengono archiviati come valori di WORD. È possibile archiviare un valore integer come valore DWORD qualificando l'Integer con il suffisso "L".

Le stringhe sono racchiuse tra virgolette. RC non aggiunge automaticamente un carattere di terminazione null a una stringa. Ogni stringa è una sequenza dei caratteri ANSI specificati, a meno che non venga qualificata come stringa di caratteri wide con il prefisso "L".

Il blocco di dati inizia in un limite **DWORD** e RC non esegue la spaziatura interna o l'allineamento dei dati all'interno del blocco di *dati non elaborati* . È responsabilità del programmatore garantire l'allineamento corretto dei dati all'interno del blocco.

</dd> </dl>

## <a name="example"></a>Esempio

Nell'esempio seguente vengono illustrate diverse istruzioni definite dall'utente:

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




