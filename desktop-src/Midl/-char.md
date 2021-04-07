---
title: opzione/char
description: L'opzione/char consente di garantire che il compilatore MIDL e il compilatore C funzionino insieme correttamente per tutti i tipi char e Small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char switch MIDL
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718703"
---
# <a name="char-switch"></a>opzione/char

L'opzione **/char** consente di garantire che il compilatore MIDL e il compilatore C funzionino insieme correttamente per tutti i tipi [**char**](char-idl.md) e [**small**](small.md) .

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span id="signed"></span><span id="SIGNED"></span>con segno * * * *


</dt> <dd>

Specifica che il tipo di compilatore C predefinito per [**char**](char-idl.md) è firmato. Tutte le occorrenze di **char** non associate a una specifica del segno vengono generate come carattere senza segno.

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span id="unsigned"></span><span id="UNSIGNED"></span>senza segno * * * *


</dt> <dd>

Specifica che il tipo di compilatore C predefinito per [**char**](char-idl.md) è senza segno. Tutti gli utilizzi di [**small**](small.md) non accompagnati da una specifica del segno vengono generati con segno di dimensioni ridotte.

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span id="ascii7"></span><span id="ASCII7"></span>ascii7 * * * *


</dt> <dd>

Specifica che tutti i valori [**char**](char-idl.md) devono essere passati nei file generati senza una parola chiave del segno specifica. Tutti gli utilizzi di [**small**](small.md) non accompagnati da una specifica del segno vengono generati come **piccoli**.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per definizione, il [**carattere**](char-idl.md) MIDL è senza segno. "Small" è definito in termini di **char** ( \# define Small Char) e MIDL [**small**](small.md) è firmato.

L'opzione **/char** indica al compilatore MIDL di specificare dichiarazioni esplicite o non [**firmate**](unsigned.md) nei file generati quando la dichiarazione di firma del compilatore C è in conflitto con l'impostazione predefinita MIDL per quel tipo. [](signed.md)

Tenere presente che il compilatore MIDL genera gli stub come codice sorgente C, che è necessario compilare come parte dei programmi client e server. Alcuni compilatori usano i dati [**char**](char-idl.md) con **segno** ovunque nel codice sorgente. Il codice sorgente dello stub che il compilatore MIDL genera considera tutti i dati **char** come **unsigned char**. Se il compilatore MIDL genera semplicemente tutti i dati **char** nel file IDL come dati **char** negli Stub, i compilatori che usano un **carattere signed** per i dati **char** potrebbero causare un conflitto nel codice sorgente dello stub.

Lo scopo dell'opzione della riga di comando **/char** è risolvere questi potenziali conflitti. Conserva tutti i dati specificati come [**caratteri**](char-idl.md) nel file IDL come **carattere senza segno** nel codice sorgente dello stub. Gestisce anche [**piccoli**](small.md) dati come firmati.

Nella tabella seguente vengono riepilogati i tipi generati.



| MIDL/char-opzione       | Tipo char generato | Tipo piccolo generato |
|-------------------------|---------------------|----------------------|
| **/char MIDL firmato**   | **unsigned char**   | **small**            |
| **MIDL/char senza segno** | **char**            | **con segno piccolo**     |
| **ascii7/char MIDL**   | **char**            | **small**            |



 

L'opzione **/char** signed indica che i tipi char e Small del compilatore C sono firmati. Per trovare la corrispondenza con il valore predefinito MIDL per **char**, il compilatore MIDL deve convertire tutti gli usi di **char** non accompagnati da una specifica di segno a un **carattere senza segno**. Il tipo [**piccolo**](small.md) non viene modificato perché questa impostazione predefinita del compilatore C corrisponde al valore predefinito MIDL per **small**.

L'opzione unsigned **/char** indica che il tipo [**char**](char-idl.md) del compilatore C è senza segno. Il compilatore MIDL converte tutti gli utilizzi di [**small**](small.md) non accompagnati da una specifica di **segno a** **small** con segno.

L'opzione ascii7 indica che non viene aggiunta alcuna specifica di firma esplicita ai tipi [**char**](char-idl.md) . Il tipo [**small**](small.md) viene generato come **small**.

Per evitare confusione, è consigliabile utilizzare le specifiche esplicite del segno per i tipi [**char**](char-idl.md) e Small quando possibile nel file IDL. Si noti che l'uso di tipi **char** con firma esplicita nel file IDL non è supportato da DCE IDL. Pertanto, questa funzionalità non è disponibile quando si esegue la compilazione con l'opzione MIDL [**/OSF**](-osf.md) .

Per ulteriori informazioni relative a **/char**, vedere [**small**](small.md).

## <a name="examples"></a>Esempio

**nome file. idl con firma MIDL/char**

**MIDL/char unsigned filename. idl**

**MIDL/char ascii7 nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**char**](char-idl.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**piccolo**](small.md)
</dt> </dl>

 

 




