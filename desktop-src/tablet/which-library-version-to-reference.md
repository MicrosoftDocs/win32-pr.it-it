---
description: In questo argomento vengono descritte le differenze tra le versioni binarie della libreria Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Versione della libreria a cui fare riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899866dd11bbe72f9476ee3b645ed4e5612fe7043dae38675bd206e81562ca68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589281"
---
# <a name="which-library-version-to-reference"></a>Versione della libreria a cui fare riferimento

In questo argomento vengono descritte le differenze tra le versioni binarie della libreria Tablet PC.

## <a name="tablet-pc-library-versions"></a>Versioni della libreria Tablet PC

I file binari della libreria tablet PC (Microsoft.Ink.dll) sono stati aggiornati in Windows Vista. I file binari di queste versioni vengono definiti "versione 6.0" per co-incidere con la versione di Windows in cui vengono rilasciati.

La versione più recente dei file binari compatibili con Windows XP è definita "versione 1.7".

L Windows SDK può essere installato nei computer Vista e XP e Windows SDK include entrambe le versioni di Microsoft.Ink.dll.

Questi sono installati in:

1. %programfiles% \\ Reference Assemblies \\ Microsoft Tablet PC \\ \\ v1.7 \\Microsoft.Ink.dll

2. %programfiles% \\ Reference Assemblies \\ Microsoft Tablet PC \\ \\ v6.0 \\Microsoft.Ink.dll

I file binari della versione 6.0 sono compatibili solo con Windows Vista e le applicazioni scritte su di essi devono essere eseguite solo in Windows Vista.

Un'applicazione scritta sui file binari della versione 1.7 deve essere eseguita senza modifiche se installata Windows Vista.

 

 



