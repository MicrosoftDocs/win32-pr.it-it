---
description: ICE70 verifica che i valori integer per le voci del registro di sistema siano specificati correttamente.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315469"
---
# <a name="ice70"></a>ICE70

ICE70 verifica che i valori integer per le voci del registro di sistema siano specificati correttamente. I valori nel formato \# \# Str, \# % unexpanded Str non vengono convalidati. \#Vengono convalidati i valori nel formato xhex, \# xhex, \# Integer e \# \[ Property \] . La tabella seguente fornisce una breve panoramica.



| Valore                 | Convalida                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| \#\#Str               | valido                                                                         |
| \#% Str non espansa     | valido                                                                         |
| \#xHex, \# xHex         | Verificare la presenza di caratteri esadecimali validi (da 0 a 9, a-f, A-F). Le proprietà sono consentite qui. |
| \#+ int, \# -int, \# int | Verificare la presenza di caratteri numerici validi (0-9). Le proprietà sono consentite qui.     |



 

La sintassi per un valore integer da immettere nel registro di sistema è \# Integer in cui Integer è numerico.

## <a name="result"></a>Risultato

ICE70 segnala un errore se i valori integer per le voci del registro di sistema non sono specificati correttamente.

## <a name="example"></a>Esempio

ICE70 segnala gli errori seguenti per l'esempio specificato.

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

Per correggere l'errore: se si desidera che il valore sia numerico, modificare il valore in modo da utilizzare tutti i caratteri numerici. Se si desidera che il valore sia una stringa, deve essere preceduto da due ' \# ' ( \# \# ) anziché uno solo.

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

Per correggere l'errore: i caratteri esadecimali validi sono 0-9, A-F e a-f. Solo questi caratteri possono seguire la \# x (o \# x).

[Tabella del registro di sistema](registry-table.md) (parziale)



| Registro | Valore    |
|----------|----------|
| Reg1     | \#12xz34 |
| Reg2     | \#xz34   |



 

## <a name="remarks"></a>Commenti

-   \#\[proprietà \] valida.
-   \#\[Proprietà non valida (parentesi di chiusura mancante).
-   \#\[\] \[ myprop2 myprop1 è valido. (Anche se l'ultimo manca la parentesi finale, myprop1 potrebbe restituire Str, in \# modo da avere \# \# Str \[ myprop2, che è valido
-   \#\]proprietà \[ non valida
-   Qualsiasi proprietà incorporata in una stringa valore non può trovarsi nel \[ \] form $compkey, \[ \# FileKey \] o \[ ! FileKey \] perché non sono numerici. Tuttavia, esiste un'eccezione, la \# \[ proprietà \] \[ $compkey \] (o \[ \# FileKey \] o \[ ! FileKey \] ) è valida perché, come nel precedente, la \[ proprietà \] può restituire \# Str.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



