---
title: Opzione /char
description: L'opzione /char consente di garantire che il compilatore MIDL e il compilatore C funzionino correttamente insieme per tutti i tipi char e small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- Opzione /char MIDL
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb459f7c2d6ff98a35e139cf07d9d95c4bed575e52b3d20258f570f07297943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963191"
---
# <a name="char-switch"></a>Opzione /char

**L'opzione /char** consente di garantire che il compilatore MIDL e il compilatore C funzionino correttamente insieme per tutti [**i tipi char**](char-idl.md) e [**small.**](small.md)

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span id="signed"></span><span id="SIGNED"></span>signed****


</dt> <dd>

Specifica che il tipo di compilatore C predefinito per [**char**](char-idl.md) è firmato. Tutte le occorrenze **di char** non accompagnate da una specifica di segno vengono generate come caratteri senza segno.

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span id="unsigned"></span><span id="UNSIGNED"></span>unsigned****


</dt> <dd>

Specifica che il tipo predefinito del compilatore C per [**char**](char-idl.md) è senza segno. Tutti gli usi [**di piccole**](small.md) dimensioni non accompagnati da una specifica di segno vengono generati come piccoli firmati.

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span id="ascii7"></span><span id="ASCII7"></span>ascii7****


</dt> <dd>

Specifica che tutti i [**valori char**](char-idl.md) devono essere passati nei file generati senza una parola chiave di segno specifica. Tutti gli usi [**di piccole**](small.md) dimensioni non accompagnati da una specifica di segno vengono generati come **piccoli**.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per definizione, il carattere [**MIDL**](char-idl.md) è senza segno. "Small" è definito in termini di **char** ( \# define small char) e MIDL [**small**](small.md) è con segno.

L'opzione **/char** indica al compilatore [](signed.md) MIDL di specificare dichiarazioni esplicite con segno o senza segno nei file generati quando la dichiarazione del segno del compilatore C è in conflitto con l'impostazione predefinita MIDL per tale tipo. [](unsigned.md)

Tenere presente che il compilatore MIDL genera gli stub come codice sorgente C, che è necessario compilare come parte dei programmi client e server. Alcuni compilatori usano un **carattere con segno** ovunque i dati [**char**](char-idl.md) vengono specificati nel codice sorgente. Il codice sorgente stub generato dal compilatore MIDL considera tutti i dati **char** **come unsigned char**. Se il compilatore MIDL ha semplicemente generato tutti i dati **char** nel file  IDL come dati **char** negli stub, i compilatori che usano un char con segno per i dati **char** causerebbero un conflitto nel codice sorgente dello stub.

Lo scopo **dell'opzione della riga** di comando /char è risolvere questi potenziali conflitti. Mantiene tutti i dati specificati come [**char nel**](char-idl.md) file IDL come char **senza segno** nel codice sorgente dello stub. Gestisce anche dati [**di piccole dimensioni**](small.md) come firmati.

Nella tabella seguente sono riepilogati i tipi generati.



| Opzione midl /char       | Tipo char generato | Tipo piccolo generato |
|-------------------------|---------------------|----------------------|
| **midl /char signed**   | **unsigned char**   | **small**            |
| **midl /char senza segno** | **char**            | **signed small**     |
| **midl /char ascii7**   | **char**            | **small**            |



 

**L'opzione /char** signed indica che i tipi char e small del compilatore C sono firmati. Per trovare la corrispondenza con l'impostazione predefinita MIDL per **char**, il compilatore MIDL deve convertire tutti gli usi di **char** non accompagnati da una specifica di segno in **unsigned char**. Il [**tipo piccolo**](small.md) non viene modificato perché il valore predefinito del compilatore C corrisponde all'impostazione predefinita MIDL per **small**.

**L'opzione /char** unsigned indica che il tipo char del [**compilatore**](char-idl.md) C è senza segno. Il compilatore MIDL converte tutti gli usi di [**small**](small.md) non accompagnati da una specifica di segno in **con segno** **small**.

L'opzione ascii7 indica che non viene aggiunta alcuna specifica di segno esplicito ai [**tipi char.**](char-idl.md) Il tipo [**small**](small.md) viene generato come **small**.

Per evitare confusione, è consigliabile usare specifiche di segno esplicito per i tipi [**char**](char-idl.md) e small quando possibile nel file IDL. Si noti che l'uso di tipi **char** firmati in modo esplicito nel file IDL non è supportato da DCE IDL. Pertanto, questa funzionalità non è disponibile quando si esegue la compilazione con l'opzione [**MIDL /osf.**](-osf.md)

Per altre informazioni relative a **/char**, vedere [**small**](small.md).

## <a name="examples"></a>Esempio

**midl /char signed filename.idl**

**midl /char unsigned filename.idl**

**midl /char ascii7 filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Piccolo**](small.md)
</dt> </dl>

 

 




