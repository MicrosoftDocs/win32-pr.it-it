---
title: cpp_quote (attributo)
description: La \_ parola chiave delle virgolette cpp indica a MIDL di emettere la stringa specificata, senza virgolette, nel file di intestazione generato.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- attributo cpp_quote MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045862"
---
# <a name="cpp_quote-attribute"></a>\_attributo di virgolette cpp

La parola chiave delle **\_ virgolette cpp** indica a MIDL di emettere la stringa specificata, senza virgolette, nel file di intestazione generato.

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*string* 
</dt> <dd>

Specifica una stringa racchiusa tra virgolette emessa nel file di intestazione generato. La stringa deve essere racchiusa tra virgolette per impedire l'espansione da parte del preprocessore C.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le direttive di pre-elaborazione del linguaggio c visualizzate nel file IDL vengono elaborate dal preprocessore del compilatore C. Le direttive **\# define** nel file IDL sono disponibili durante la compilazione MIDL, ma non sono disponibili per il compilatore C.

Ad esempio, quando il preprocessore rileva la direttiva " \# define Windows 4", il preprocessore sostituisce tutte le occorrenze di "Windows" nel file IDL con "4". Il simbolo "WINDOWS" non è disponibile durante la compilazione in linguaggio C.

Per consentire alle definizioni di macro del preprocessore C di passare attraverso il compilatore MIDL al compilatore C, usare la direttiva **\# pragma MIDL \_ echo** o **cpp \_ quot** . Queste direttive indicano al compilatore MIDL di generare un file di intestazione contenente la stringa di parametro con le virgolette rimosse. Le direttive di **\_ virgolette** Echo e cpp di **\# pragma MIDL \_** sono equivalenti.

Il compilatore MIDL inserisce le stringhe specificate nell' **\_ offerta cpp** e le direttive [**pragma**](pragma.md) nel file di intestazione nella sequenza in cui sono specificate nel file IDL e in relazione ad altri componenti dell'interfaccia nel file IDL. Le stringhe dovrebbero in genere essere visualizzate nella sezione corpo dell'interfaccia del file IDL dopo tutte le operazioni di [**importazione**](import.md) .

## <a name="examples"></a>Esempi

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importare**](import.md)
</dt> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




