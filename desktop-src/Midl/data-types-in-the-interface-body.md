---
title: Tipi di dati nel corpo dell'interfaccia
description: Il corpo dell'interfaccia racchiuso tra parentesi graffe () contiene i tipi di dati che verranno utilizzati nelle chiamate a procedure remote e nei prototipi per le funzioni che verranno eseguite in modalità remota.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- interfacce MIDL, tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297979"
---
# <a name="data-types-in-the-interface-body"></a>Tipi di dati nel corpo dell'interfaccia

Il corpo dell'interfaccia racchiuso tra parentesi graffe ({}) contiene i tipi di dati che verranno utilizzati nelle chiamate a procedure remote e nei prototipi per le funzioni che verranno eseguite in modalità remota. Il corpo di un'interfaccia può contenere importazioni, pragma, dichiarazioni di costanti, dichiarazioni di tipo e dichiarazioni di funzione. Fatta eccezione per la modalità di compatibilità OSF, il compilatore MIDL consente anche dichiarazioni implicite sotto forma di definizioni di variabili.

Si noti che la specifica OSF-DCE per le interfacce RPC non consente più interfacce in un unico file IDL. Pertanto, se si esegue la compilazione in modalità di compatibilità OSF ( [**/OSF**](-osf.md)) di MIDL, il file IDL può contenere una sola interfaccia.

Per informazioni dettagliate sull'uso del compilatore MIDL per produrre librerie dei tipi, vedere [generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md).

In Microsoft RPC, un file IDL può contenere più interfacce e queste interfacce possono essere dichiarate in modo diretto (all'interno del file IDL che le definisce). Ad esempio:

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




