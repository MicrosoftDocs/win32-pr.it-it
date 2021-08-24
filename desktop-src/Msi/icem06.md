---
description: ICEM06 verifica la presenza di riferimenti diretti non validi alle funzionalità da parte del modulo.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5150e511e6f8018e51ab537b52ccc6c32645d09c80110129f040d6a329335ec5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828881"
---
# <a name="icem06"></a>ICEM06

ICEM06 verifica la presenza di riferimenti diretti non validi alle funzionalità da parte del modulo.

Gli ICE del modulo unione vengono archiviati in un file CUB del modulo merge denominato Mergemod.cub e non nel file con estensione cub contenente gli ICO usati per la convalida dei pacchetti.

## <a name="result"></a>Risultato

ICEM06 invia un errore quando il database del modulo contiene riferimenti diretti a una funzionalità. Le informazioni sulle funzionalità devono essere fornite dall'utente del modulo.

## <a name="example"></a>Esempio

ICEM06 pubblica i messaggi di errore seguenti per un modulo contenente le voci di database illustrate di seguito.

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida          | Destinazione                                 |
|-------------------|----------------------------------------|
| Collegamento1. *GUID1* | cmd.exe                                |
| Collegamento2. *GUID1* | \[MyProp\]                             |
| Collegamento3. *GUID1* | {00000000-0000-0000-0000-000000000000} |



 

[Tabella di classi](class-table.md) (parziale)



| CLSID   | Contesto       | Componente\_ | Funzionalità\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Componente1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Componente2  | Funzionalità                              |



 

ICEM06 segnala il primo errore perché il primo record nella tabella Collegamento contiene una voce nel campo Destinazione che non è una proprietà o un GUID Null. Un modulo non può fare riferimento direttamente a una funzionalità. Le informazioni sulle funzionalità devono essere fornite dall'utente del modulo. Per correggere l'errore, i riferimenti a una funzionalità devono essere sostituiti da un GUID Null.

ICEM06 segnala il secondo errore perché il secondo record nella tabella Class contiene una voce nel campo Feature che non è un GUID Null. Un modulo non può fare riferimento direttamente a una funzionalità. Le informazioni sulle funzionalità devono essere fornite dall'utente del modulo. Per correggere l'errore, i riferimenti a una funzionalità devono essere sostituiti da un GUID Null.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



