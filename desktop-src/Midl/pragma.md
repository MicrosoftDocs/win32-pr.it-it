---
title: pragma (attributo)
description: La direttiva \ pragma MIDL \_ echo indica a MIDL di emettere la stringa specificata, senza virgolette, nel file di intestazione generato.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- attributo pragma MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955879"
---
# <a name="pragma-attribute"></a>pragma (attributo)

La \# direttiva **pragma MIDL \_ echo** indica a MIDL di emettere la stringa specificata, senza virgolette, nel file di intestazione generato.

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

Specifica una sequenza di token che vengono inseriti nel file di intestazione generato come parte di una direttiva **\# pragma** senza elaborazione da parte del compilatore MIDL.

</dd> <dt>

*n* 
</dt> <dd>

Specifica la dimensione corrente del pacchetto. Tra i valori validi sono compresi 1, 2, 4, 8 e 16.

</dd> <dt>

*id* 
</dt> <dd>

Specifica l'identificatore utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le direttive di pre-elaborazione del linguaggio c visualizzate nel file IDL vengono elaborate dal preprocessore del compilatore C. Le direttive **\# define** nel file IDL sono disponibili durante la compilazione MIDL, anche se non al compilatore C.

Ad esempio, quando il preprocessore rileva la direttiva " \# define Windows 4", il preprocessore sostituisce tutte le occorrenze di "Windows" nel file IDL con "4". Il simbolo "WINDOWS" non è disponibile in fase di compilazione C.

Per consentire alle definizioni di macro del preprocessore C di passare attraverso il compilatore MIDL al compilatore C, usare la direttiva **\# pragma MIDL \_ echo** o [**cpp \_ quot**](cpp-quote.md) . Queste direttive indicano al compilatore MIDL di generare un file di intestazione contenente la stringa di parametro con le virgolette rimosse. Le direttive di **\_ virgolette** Echo e cpp di **\# pragma MIDL \_** sono equivalenti.

La direttiva **\# pragma pack** viene usata dal compilatore MIDL per controllare la compressione delle strutture. Esegue l'override dell'opzione della riga di comando [**/ZP**](-zp.md) . L'opzione Pack (*n*) consente di impostare le dimensioni correnti del pacchetto su un valore specifico: 1, 2, 4, 8 o 16. Le opzioni Pack (push) e Pack (pop) presentano le caratteristiche seguenti:

-   Il compilatore mantiene uno stack di compressione. Gli elementi dello stack di compressione includono una dimensione del pacchetto e un *ID* facoltativo. Lo stack è limitato solo dalla memoria disponibile con le dimensioni del pacchetto corrente nella parte superiore dello stack.
-   Pack (push) determina la dimensione corrente del pacchetto inserita nello stack di compressione. Lo stack è limitato dalla memoria disponibile.
-   Pack (push,*n*) corrisponde a Pack (push) seguito da Pack (*n*).
-   Pack (push, *ID*) inserisce anche l' *ID* nello stack di compressione insieme alle dimensioni del pacchetto.
-   Pack (push, *ID*, *n*) corrisponde a Pack (push, *ID*) seguito da Pack (*n*).
-   Pack (pop) genera lo stack di compressione. I pop sbilanciati generano avvisi e impostano le dimensioni correnti del pacchetto sul valore della riga di comando.
-   Se si specifica Pack (pop, *ID*, *n*), *n* viene ignorato.

Il compilatore MIDL inserisce le stringhe specificate nell' [**\\ \_ offerta cpp**](cpp-quote.md) e le direttive **pragma** nel file di intestazione nella sequenza in cui sono specificate nel file IDL e in relazione ad altri componenti dell'interfaccia nel file IDL. Le stringhe dovrebbero in genere essere visualizzate nella sezione Interface-Body del file IDL dopo tutte le operazioni di [**importazione**](import.md) .

Il compilatore MIDL non tenta di elaborare direttive **\# pragma** che non iniziano con il prefisso "MIDL" \_ . Altre direttive **\# pragma** nel file IDL vengono passate nel file di intestazione generato senza modifiche.

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

[**\_virgolette cpp**](cpp-quote.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importare**](import.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




