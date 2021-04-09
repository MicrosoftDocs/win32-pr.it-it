---
description: ICEM06 verifica la presenza di riferimenti diretti non validi alle funzionalità da parte del modulo.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882406"
---
# <a name="icem06"></a>ICEM06

ICEM06 verifica la presenza di riferimenti diretti non validi alle funzionalità da parte del modulo.

I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.

## <a name="result"></a>Risultato

ICEM06 Invia un errore quando il database del modulo contiene riferimenti diretti a una funzionalità. Le informazioni sulle funzionalità devono essere fornite dall'utente del modulo.

## <a name="example"></a>Esempio

ICEM06 invia i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida          | Destinazione                                 |
|-------------------|----------------------------------------|
| Shortcut1. *Guid1* | cmd.exe                                |
| Shortcut2. *Guid1* | \[Prop\]                             |
| Shortcut3. *Guid1* | {00000000-0000-0000-0000-000000000000} |



 

[Tabella classi](class-table.md) (parziale)



| CLSID   | Context       | Componente\_ | Funzionalità\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Component1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Component2  | Funzionalità di                              |



 

ICEM06 segnala il primo errore perché il primo record nella tabella dei collegamenti include una voce nel campo di destinazione che non è una proprietà o un GUID null. Un modulo non può fare riferimento direttamente a una funzionalità. Le informazioni sulle funzionalità devono essere fornite dall'utente del modulo. Per correggere l'errore, i riferimenti a una funzionalità devono essere sostituiti da un GUID null.

ICEM06 segnala il secondo errore perché il secondo record nella tabella della classe include una voce nel campo della funzionalità che non è un GUID null. Un modulo non può fare riferimento direttamente a una funzionalità. Le informazioni sulle funzionalità devono essere fornite dall'utente del modulo. Per correggere l'errore, i riferimenti a una funzionalità devono essere sostituiti da un GUID null.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



