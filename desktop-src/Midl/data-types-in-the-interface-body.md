---
title: Tipi di dati nel corpo dell'interfaccia
description: Il corpo dell'interfaccia, racchiuso tra parentesi graffe ( ), contiene i tipi di dati che verranno usati nelle chiamate di procedura remota e nei prototipi per le funzioni che verranno eseguite in remoto.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- interfacce MIDL, tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6691ccf89e1bff3b0e980678a30c6f706b724e4f30192d7960183c00cc00c237
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979710"
---
# <a name="data-types-in-the-interface-body"></a>Tipi di dati nel corpo dell'interfaccia

Il corpo dell'interfaccia, racchiuso tra parentesi graffe ({ }), contiene i tipi di dati che verranno usati nelle chiamate di procedura remota e nei prototipi per le funzioni che verranno eseguite in remoto. Un corpo dell'interfaccia può contenere importazioni, pragma, dichiarazioni di costanti, dichiarazioni di tipo e dichiarazioni di funzione. Ad eccezione della modalità di compatibilità OSF, il compilatore MIDL consente anche dichiarazioni implicite sotto forma di definizioni di variabili.

Si noti che la specifica OSF-DCE per le interfacce RPC non consente più interfacce in un singolo file IDL. Pertanto, se si esegue la compilazione in modalità di compatibilità OSF di MIDL ( [**/osf**](-osf.md)), il file IDL può contenere una sola interfaccia.

Per informazioni dettagliate sull'uso del compilatore MIDL per produrre librerie dei tipi, vedere [Generazione di una libreria dei tipi con MIDL.](generating-a-type-library-with-midl-2.md)

In Microsoft RPC, un file IDL può contenere più interfacce e queste interfacce possono essere dichiarate in avanti (all'interno del file IDL che le definisce). Ad esempio:

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

 

 




