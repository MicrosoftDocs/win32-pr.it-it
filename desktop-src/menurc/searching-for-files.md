---
title: Ricerca di file
description: Per impostazione predefinita, RC Cerca i file di intestazione e i file di risorse (ad esempio, i file di icona e di cursore) nella directory corrente e quindi nelle directory specificate dalla variabile di ambiente INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298631"
---
# <a name="searching-for-files"></a>Ricerca di file

Per impostazione predefinita, RC Cerca i file di intestazione e i file di risorse (ad esempio, i file di icona e di cursore) nella directory corrente e quindi nelle directory specificate dalla variabile di ambiente INCLUDE. La variabile di ambiente PATH non ha alcun effetto sulle ricerche nelle directory RC.

## <a name="adding-a-directory-to-search"></a>Aggiunta di una directory in cui eseguire la ricerca

È possibile usare l'opzione **/i** per aggiungere una directory all'elenco di ricerche di directory RC. Il compilatore cerca quindi le directory nell'ordine seguente:

1.  Directory corrente
2.  La directory o le directory specificate usando l'opzione **/i** nell'ordine in cui sono visualizzate nella riga di comando RC
3.  Elenco di directory specificate dalla variabile di ambiente INCLUDE, nell'ordine in cui sono elencate dalla variabile, a meno che non si specifichi l'opzione **/x**

Nell'esempio seguente viene compilato il file di definizione delle risorse MyApp. RC:

**RC/i c: \\ origine-elementi \\ /i d: \\ Resources MyApp. RC**

Quando si compila lo script MyApp. RC, RC cerca prima i file di intestazione e i file di risorse nella directory corrente, quindi in C: \\ source \\ Stuff e D: \\ Resources, quindi nelle directory specificate dalla variabile di ambiente include.

## <a name="ignoring-the-include-environment-variable"></a>La variabile di ambiente INCLUDE verrà ignorata

È possibile impedire a RC di usare la variabile di ambiente INCLUDE quando si determinano le directory in cui eseguire la ricerca. A tale scopo, usare l'opzione **/x** . Il compilatore cerca quindi i file solo nella directory corrente e in tutte le directory specificate usando l'opzione **/i** .

Il comando seguente compila il file script MyApp. RC:

**RC/x/i c: \\ materiale di origine \\ MyApp. RC**

Quando si compila lo script MyApp. RC, RC Cerca i file di intestazione e i file di risorse prima nella directory corrente e quindi in C: \\ source \\ Stuff. Non esegue la ricerca nelle directory specificate dalla variabile di ambiente INCLUDE.

 

 




