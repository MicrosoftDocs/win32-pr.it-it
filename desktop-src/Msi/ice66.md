---
description: ICE66 usa le tabelle del database per determinare lo schema che il database deve usare.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023450a451a412c47c21904ab96a13e4513c71f8327966dffa5b657b1b65bb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787401"
---
# <a name="ice66"></a>ICE66

ICE66 usa le tabelle del database per determinare lo schema che il database deve usare.

Alcune funzionalità possono essere disponibili solo se il pacchetto è installato in un sistema con una versione Windows installer.

## <a name="result"></a>Risultato

ICE66 invia un avviso se il database usa lo schema errato.

## <a name="example"></a>Esempio

ICE66 segnala l'avviso seguente per l'esempio illustrato.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

Questo avviso può essere ignorato se si vuole che il pacchetto sia installato usando una versione Windows installer. Ad esempio, se si vuole che il pacchetto sia installabile solo nella versione 2.0 o successiva, modificare lo schema del pacchetto (PID \_ PAGECOUNT) su 200.

[Tabella IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ condiviso | Applicazione \_ componente |
|-------------------|------------------------|
| Componente1        | Componente2             |



 

[Flusso di informazioni di riepilogo](summary-information-stream.md)



| PIDt           | Valore |
|----------------|-------|
| PID \_ PAGECOUNT | 100   |



 

## <a name="table-used-during-execution"></a>Tabella usata durante l'esecuzione:

[\_Tabella Columns](-columns-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



