---
title: pragma (attributo)
description: La direttiva \ pragma midl echo indica a MIDL di generare la stringa specificata, senza le \_ virgolette, nel file di intestazione generato.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- Attributo pragma MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ca869acddf4b0a0a098707833e889efcfccc267a3abf1949921c550cf66c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383499"
---
# <a name="pragma-attribute"></a>pragma (attributo)

La direttiva pragma midl echo indica a MIDL di generare la stringa specificata, senza le \# virgolette, nel file di intestazione generato. **\_**

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*string* 
</dt> <dd>

Specifica una stringa inserita nel file di intestazione generato. Le virgolette vengono rimosse durante il processo di inserimento.

</dd> <dt>

*sequenza di token* 
</dt> <dd>

Specifica una sequenza di token inseriti nel file di intestazione generato come parte di una direttiva **\# pragma** senza elaborazione da parte del compilatore MIDL.

</dd> <dt>

*n* 
</dt> <dd>

Specifica le dimensioni correnti del pacchetto. Tra i valori validi sono compresi 1, 2, 4, 8 e 16.

</dd> <dt>

*id* 
</dt> <dd>

Specifica l'identificatore utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le direttive di pre-elaborazione del linguaggio C visualizzate nel file IDL vengono elaborate dal preprocessore del compilatore C. Le **\# direttive define** nel file IDL sono disponibili durante la compilazione MIDL, anche se non per il compilatore C.

Ad esempio, quando il preprocessore rileva la direttiva " define WINDOWS 4", il preprocessore sostituisce tutte le occorrenze di \# "WINDOWS" nel file IDL con "4". Il simbolo "WINDOWS" non è disponibile in fase di compilazione C.

Per consentire alle definizioni di macro del preprocessore C di passare il compilatore MIDL al compilatore C, usare la direttiva **\# pragma midl \_ echo** o [**cpp \_ quote.**](cpp-quote.md) Queste direttive indicano al compilatore MIDL di generare un file di intestazione contenente la stringa di parametro con le virgolette rimosse. Le **\# direttive pragma midl \_ echo** **e cpp \_ quote** sono equivalenti.

La **\# direttiva pragma pack** viene usata dal compilatore MIDL per controllare la creazione di un pacchetto di strutture. Esegue l'override dell'opzione della riga di comando [**/Zp.**](-zp.md) L'opzione pack (*n*) imposta le dimensioni correnti del pacchetto su un valore specifico: 1, 2, 4, 8 o 16. Le opzioni pack (push) e pack (pop) hanno le caratteristiche seguenti:

-   Il compilatore gestisce uno stack di creazione di un pacchetto. Gli elementi dello stack di creazione di un pacchetto includono una dimensione di tipo pack e un *ID facoltativo*. Lo stack è limitato solo dalla memoria disponibile con la dimensione pack corrente all'inizio dello stack.
-   Pack (push) comporta il push delle dimensioni di pack correnti nello stack di packing. Lo stack è limitato dalla memoria disponibile.
-   Pack (push,*n*) è uguale a pack (push) seguito da pack (*n*).
-   Pack (push, *id)* inserisce anche *l'ID* nello stack di packing insieme alle dimensioni del pacchetto.
-   Pack (push, *id*, *n*) è uguale a pack (push, *id*) seguito da pack (*n*).
-   Pack (pop) comporta l'espulso dello stack di packing. I pop sbilanciati causano avvisi e impostano le dimensioni correnti del pacchetto sul valore della riga di comando.
-   Se pack (pop, *id*, *n*) è specificato, *n* viene ignorato.

Il compilatore MIDL inserisce le stringhe specificate nelle direttive **pragma** e virgolette [**\\ cpp \_**](cpp-quote.md) nel file di intestazione nella sequenza in cui sono specificate nel file IDL e relative ad altri componenti dell'interfaccia nel file IDL. Le stringhe devono in genere essere visualizzate nella sezione interface-body del file IDL dopo tutte le [**operazioni di**](import.md) importazione.

Il compilatore MIDL non tenta di elaborare **\# direttive pragma** che non iniziano con il prefisso "midl \_ ". Altre **\# direttive pragma** nel file IDL vengono passate nel file di intestazione generato senza modifiche.

## <a name="examples"></a>Esempi

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Citazione \_ cpp**](cpp-quote.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Importazione**](import.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




