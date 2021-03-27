---
title: " line (direttiva)"
description: Direttiva per il preprocessore che imposta il numero di riga e il nome file archiviati internamente del compilatore sui valori specificati.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- HLSL (direttiva riga)
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397666"
---
# <a name="line-directive"></a>\#line (direttiva)

Direttiva per il preprocessore che imposta il numero di riga e il nome file archiviati internamente del compilatore sui valori specificati.



| \#riga *lineNumber* "*nomefile*" |
|----------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                              | Descrizione                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*<br/>                    | Numero di riga da impostare. Può trattarsi di qualsiasi costante di tipo Integer. È possibile eseguire la sostituzione delle macro sui token di pre-elaborazione, purché il risultato restituisca la sintassi corretta. <br/>                     |
| <span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*nome file* \[ opzionale\] <br/> | Nome file da impostare. Il nome file può essere costituito da qualsiasi combinazione di caratteri e deve essere racchiuso tra virgolette doppie (""). Se questo parametro viene omesso, il nome del file precedente rimane invariato. <br/> |



 

## <a name="remarks"></a>Commenti

Il compilatore usa il numero di riga e il nome del file per fare riferimento agli errori rilevati durante la compilazione. Il numero di riga in genere si riferisce alla linea di input corrente, mentre il nome del file fa riferimento al file di input corrente. Il numero di riga viene incrementato dopo l'elaborazione di ogni riga. Se si modifica il numero di riga e il nome del file, il compilatore ignora i valori precedenti e continua l'elaborazione con i nuovi valori. La \# direttiva line viene in genere utilizzata dai generatori di programma per fare in modo che i messaggi di errore facciano riferimento al file di origine originale anziché al programma generato.

Il convertitore usa il numero di riga e il nome file per determinare i valori del \_ \_ file \_ \_ e della \_ \_ riga \_ \_ delle macro predefinite. È possibile utilizzare queste macro per inserire messaggi di errore autodescrittivi nel testo del programma. La \_ \_ macro file si \_ \_ espande in una stringa il cui contenuto è il nome file, racchiuso tra virgolette doppie ("").

## <a name="examples"></a>Esempio

Nell'esempio seguente il numero di riga viene impostato su 151 e il nome del file viene impostato su "copy. c".


```
#line 151 "copy.c"
```



Nell'esempio seguente, la macro ASSERT usa la riga e il file delle macro predefinite \_ \_ \_ \_ \_ \_ \_ \_ per stampare un messaggio di errore relativo al file di origine se l'asserzione specificata non è true.


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





