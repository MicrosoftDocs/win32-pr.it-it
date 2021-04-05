---
title: Generazione UUID dell'interfaccia
description: Generazione di identificatori univoci universali (UUID) dell'interfaccia e uso di uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710204"
---
# <a name="generating-interface-uuids"></a>Generazione UUID dell'interfaccia

Questa sezione presenta informazioni sugli identificatori univoci (UUID) universali e l'utilità uuidgen negli argomenti seguenti:

-   [Che cos'è un UUID?](#what-is-a-uuid)
-   [Uso di uuidgen](#using-uuidgen)

## <a name="what-is-a-uuid"></a>Che cos'è un UUID?

Tutte le interfacce devono essere identificate in modo univoco in una rete, in modo che i client possano trovarle. Nelle reti di piccole dimensioni, il nome dell'interfaccia da solo può essere sufficiente per identificarlo. Tuttavia, ciò non è in genere possibile su reti di grandi dimensioni. Pertanto, gli sviluppatori in genere assegnano a ogni interfaccia un identificatore univoco universale (UUID, interscambiabile con il termine GUID o identificatore univoco globale). Un UUID è una stringa che contiene un set di cifre esadecimali. Ogni interfaccia ha un UUID diverso. Per informazioni dettagliate, vedere [UUID di stringa](string-uuid.md).

La rappresentazione testuale di un UUID è una stringa costituita da 8 cifre esadecimali seguite da un trattino, seguite da tre gruppi delimitati da trattini di 4 cifre esadecimali, seguite da un trattino, seguite da 12 cifre esadecimali. L'esempio seguente è una stringa UUID valida:

ba209999-0c6c-11d2-97cf-00c04f8eea45

Gli UUID vuoti sono denominati UUID Nil anziché UUID **null** . Il termine Nil indica qualsiasi elemento che sia zero, vuoto, vuoto o non inizializzato. Una stringa vuota, un record di database vuoto o un UUID non inizializzato sono tutti esempi di valori Nil.

> [!Note]  
> Il valore **null** è il valore specifico zero. Viene spesso usato nella programmazione C e C++ insieme ai puntatori. Nil è un termine più generico rispetto a **null**. Gli UUID dell'interfaccia oggetto non inizializzati devono essere sempre definiti UUID Nil anziché UUID **null** .

 

## <a name="using-uuidgen"></a>Uso di uuidgen

Microsoft fornisce un programma di utilità denominato uuidgen per generare gli UUID. L'utilità uuidgen genera l'UUID nel formato di file IDL o nel formato del linguaggio C.

Quando si esegue l'utilità uuidgen dalla riga di comando, è possibile usare le opzioni di comando seguenti.



| Opzione uuidgen           | Descrizione                                                                |
|--------------------------|----------------------------------------------------------------------------|
| **/I**                   | Restituisce UUID a un modello di interfaccia IDL.                                 |
| **/s**                   | Restituisce UUID come struttura C inizializzata.                                |
| **/o** < *nome file*> | Reindirizza l'output a un file. specificata immediatamente dopo l'opzione **/o** . |
| **/n** < *numero* di>   | Specifica il numero di UUID da generare.                                 |
| **/v**                   | Visualizza le informazioni sulla versione di uuidgen.                                |
| **/h** o **?**          | Visualizza il riepilogo delle opzioni di comando.                                           |



 

In genere, si userà l'utilità uuidgen, come illustrato nell'esempio seguente.

**uuidgen-i-oMyApp. idl**

Questo comando genera un UUID e lo archivia in un file MIDL che è possibile usare come modello. Quando viene eseguito il comando precedente, il contenuto di MyApp. idl è simile al seguente:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Il passaggio successivo consiste nel sostituire il nome del segnaposto, InterfaceName, con il nome effettivo dell'interfaccia.

 

 




