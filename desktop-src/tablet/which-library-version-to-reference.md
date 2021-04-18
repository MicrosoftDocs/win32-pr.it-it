---
description: In questo argomento vengono descritte le differenze tra le versioni binarie della libreria Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Versione della libreria a cui fare riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306703"
---
# <a name="which-library-version-to-reference"></a>Versione della libreria a cui fare riferimento

In questo argomento vengono descritte le differenze tra le versioni binarie della libreria Tablet PC.

## <a name="tablet-pc-library-versions"></a>Versioni della libreria di Tablet PC

I file binari della libreria Tablet PC (Microsoft.Ink.dll) sono stati aggiornati in Windows Vista. Questi file binari sono detti "versione 6,0" per la co-incide con la versione di Windows in cui vengono rilasciati.

La versione più recente dei file binari compatibili con Windows XP è detta "versione 1,7".

Il Windows SDK può essere installato nei computer con vista e XP e il Windows SDK include entrambe le versioni di Microsoft.Ink.dll.

Sono installati in:

1. % programmi% \\ assembly di riferimento \\ Microsoft \\ Tablet \\ PC v 1.7 \\Microsoft.Ink.dll

2. % programmi% \\ assembly di riferimento \\ Microsoft \\ Tablet \\ PC v 6.0 \\Microsoft.Ink.dll

I file binari della versione 6,0 sono compatibili solo con Windows Vista e le applicazioni scritte su di essi devono essere eseguite solo in Windows Vista.

Un'applicazione scritta con i file binari della versione 1,7 dovrebbe essere eseguita senza modifiche se installata in Windows Vista.

 

 



