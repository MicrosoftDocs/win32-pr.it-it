---
title: User-Defined risorsa
description: Un'istruzione di definizione delle risorse definita dall'utente definisce una risorsa che contiene dati specifici dell'applicazione.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- risorsa definita dall'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b383b7c4d1f9acfc4ce6c9db24efa77f3bfed943c1f299186d42a1facee2b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472618"
---
# <a name="user-defined-resource"></a>User-Defined risorsa

Un'istruzione di definizione delle risorse definita dall'utente definisce una risorsa che contiene dati specifici dell'applicazione. I dati possono avere qualsiasi formato e possono essere definiti come contenuto di un determinato file (se viene specificato  il parametro *filename)* o come una serie di numeri e stringhe (se è specificato il blocco di dati non elaborati).

``` syntax
nameID typeID filename
```

Il *nome* file specifica il nome di un file contenente i dati binari della risorsa. Il contenuto del file viene incluso come risorsa. RC non interpreta i dati binari in alcun modo. È responsabilità del programmatore assicurarsi che i dati siano allineati correttamente per l'architettura del computer di destinazione.

Una risorsa definita dall'utente può anche essere definita completamente nello script della risorsa usando la sintassi seguente:

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*Nameid*
</dt> <dd>

Nome univoco o intero senza segno a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*Typeid*
</dt> <dd>

Nome univoco o intero senza segno a 16 bit che identifica il tipo di risorsa. Se viene specificato un numero, deve essere maggiore di 255. I numeri da 1 a 255 sono riservati per i tipi di risorse ridefinito esistenti e futuri.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Nome del file che contiene i dati della risorsa. Il parametro deve essere un nome di file valido. Deve essere un percorso completo se il file non si trova nella directory di lavoro corrente.

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*dati non elaborati*
</dt> <dd>

Dati non elaborati costituiti da uno o più numeri interi o stringhe di caratteri. I numeri interi possono essere specificati in formato decimale, ottale o esadecimale. Per essere compatibili con le versioni a 16 bit Windows, i numeri interi vengono archiviati come valori WORD. È possibile archiviare un numero intero come valore DWORD qualificando l'intero con il suffisso "L".

Le stringhe sono racchiuse tra virgolette. RC non aggiunge automaticamente un carattere Null di terminazione a una stringa. Ogni stringa è una sequenza dei caratteri ANSI specificati, a meno che non venga qualificata come stringa di caratteri wide con il prefisso "L".

Il blocco di dati inizia su un limite **DWORD** e RC non esegue la spaziatura interna o l'allineamento dei dati all'interno del *blocco di dati non* elaborati. È responsabilità del programmatore garantire l'allineamento corretto dei dati all'interno del blocco.

</dd> </dl>

## <a name="example"></a>Esempio

L'esempio seguente illustra diverse istruzioni definite dall'utente:

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

 

 




