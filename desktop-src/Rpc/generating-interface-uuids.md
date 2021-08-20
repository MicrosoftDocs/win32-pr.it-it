---
title: Generazione di UUID dell'interfaccia
description: Generazione di UUID (Universal Unique Identifier) dell'interfaccia e uso di Uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c21ead6161a79d000d2741a49c4fb61ff23b3a8a3340db2eb26a7805424df5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929548"
---
# <a name="generating-interface-uuids"></a>Generazione di UUID dell'interfaccia

In questa sezione vengono presentate informazioni sugli UUID (Universal Unique Identifier) e sull'utilità Uuidgen negli argomenti seguenti:

-   [Che cos'è un UUID?](#what-is-a-uuid)
-   [Uso di Uuidgen](#using-uuidgen)

## <a name="what-is-a-uuid"></a>Che cos'è un UUID?

Tutte le interfacce devono essere identificate in modo univoco in una rete in modo che i client possano trovarle. Nelle reti di piccole dimensioni, il nome dell'interfaccia può essere sufficiente per identificarla. Tuttavia, ciò non è in genere fattibile nelle reti di grandi dimensioni. Di conseguenza, gli sviluppatori assegnano in genere un UUID (Universal Unique Identifier, intercambiabile con il termine GUID o Identificatore univoco globale) a ogni interfaccia. Un UUID è una stringa che contiene un set di cifre esadecimali. Ogni interfaccia ha un UUID diverso. Per informazioni dettagliate, vedere [Stringa UUID](string-uuid.md).

La rappresentazione testuale di un UUID è una stringa costituita da 8 cifre esadecimali seguite da un trattino, seguite da tre gruppi separati da trattini di 4 cifre esadecimali, seguiti da un trattino, seguiti da 12 cifre esadecimali. L'esempio seguente è una stringa UUID valida:

ba2099999-0c6c-11d2-97cf-00c04f8eea45

Gli UUID vuoti vengono definiti UUID nil anziché **UUID NULL.** Il termine nil indica tutto ciò che è zero, vuoto, vuoto o non inizializzato. Una stringa vuota, un record di database vuoto o un UUID non inizializzato sono tutti esempi di valori null.

> [!Note]  
> Il valore **NULL** è il valore specifico zero. Viene spesso usato nella programmazione C e C++ insieme ai puntatori. Nil è un termine più generale di **NULL.** Gli UUID dell'interfaccia a oggetti non inizializzati devono sempre essere definiti UUID null anziché **UUID NULL.**

 

## <a name="using-uuidgen"></a>Uso di Uuidgen

Microsoft fornisce un programma di utilità denominato Uuidgen per generare gli UUID. L'utilità Uuidgen genera l'UUID in formato di file IDL o in formato linguaggio C.

Quando si esegue l'utilità Uuidgen dalla riga di comando, è possibile usare le opzioni di comando seguenti.



| Commutatore Uuidgen           | Descrizione                                                                |
|--------------------------|----------------------------------------------------------------------------|
| **/i**                   | Restituisce L'UUID in un modello di interfaccia IDL.                                 |
| **/s**                   | Restituisce UUID come struttura C inizializzata.                                |
| **/o** < *filename*> | Reindirizza l'output a un file. specificato immediatamente dopo **l'opzione /o.** |
| **/n** < *number*>   | Specifica il numero di UUID da generare.                                 |
| **/v**                   | Visualizza informazioni sulla versione di Uuidgen.                                |
| **/h** o **?**          | Visualizza il riepilogo dell'opzione di comando.                                           |



 

In genere si userà l'utilità Uuidgen, come illustrato nell'esempio seguente.

**uuidgen -i -oMyApp.idl**

Questo comando genera un UUID e lo archivia in un file MIDL che è possibile usare come modello. Quando viene eseguito il comando precedente, il contenuto di MyApp.idl è simile al seguente:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Il passaggio successivo consiste nel sostituire il nome segnaposto INTERFACENAME con il nome effettivo dell'interfaccia.

 

 




