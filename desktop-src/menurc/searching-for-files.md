---
title: Ricerca di file
description: Per impostazione predefinita, RC cerca i file di intestazione e i file di risorse (ad esempio file di icona e cursore) prima nella directory corrente e quindi nelle directory specificate dalla variabile di ambiente INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fecaa3c20c9bedf498c30462d5e139da83f11d45a47c6d5e7554adb8ed325b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601561"
---
# <a name="searching-for-files"></a>Ricerca di file

Per impostazione predefinita, RC cerca i file di intestazione e i file di risorse (ad esempio file di icona e cursore) prima nella directory corrente e quindi nelle directory specificate dalla variabile di ambiente INCLUDE. La variabile di ambiente PATH non ha alcun effetto sulle directory in cui RC esegue la ricerca.

## <a name="adding-a-directory-to-search"></a>Aggiunta di una directory alla ricerca

È possibile usare **l'opzione /i** per aggiungere una directory all'elenco di ricerche RC directory. Il compilatore cerca quindi le directory nell'ordine seguente:

1.  Directory corrente
2.  La directory o le directory specificate usando **l'opzione /i** nell'ordine in cui vengono visualizzate nella riga di comando RC
3.  Elenco di directory specificate dalla variabile di ambiente INCLUDE nell'ordine in cui sono elencate dalla variabile, a meno che non si specifica **l'opzione /x**

L'esempio seguente compila il file di definizione delle risorse MyApp.rc:

**rc /i c: \\ source \\ stuff /i d: \\ resources myapp.rc**

Quando si compila lo script MyApp.rc, RC cerca i file di intestazione e i file di risorse prima nella directory corrente, quindi in C: Source Stuff e D: Resources e quindi nelle directory specificate dalla variabile di ambiente \\ \\ \\ INCLUDE.

## <a name="ignoring-the-include-environment-variable"></a>Ignorare la variabile di ambiente INCLUDE

È possibile impedire a RC di usare la variabile di ambiente INCLUDE quando si determinano le directory in cui eseguire la ricerca. A tale scopo, usare **l'opzione /x.** Il compilatore cerca quindi i file solo nella directory corrente e in tutte le directory specificate usando **l'opzione /i.**

Il comando seguente compila il file di script MyApp.rc:

**rc /x /i c: \\ source \\ stuff myapp.rc**

Quando si compila lo script MyApp.rc, RC cerca i file di intestazione e di risorse prima nella directory corrente e quindi in C: \\ Source \\ Stuff. Non esegue la ricerca nelle directory specificate dalla variabile di ambiente INCLUDE.

 

 




