---
title: Surrogati DLL
description: Surrogati DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808efe4a431a703282a705000d2fe18f6b4cfcde121d95c39fe65541b0260503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993251"
---
# <a name="dll-surrogates"></a>Surrogati DLL

COM consente di creare server DLL che possono essere caricati in un processo EXE surrogato. Ciò combina la facilità di scrittura dei server DLL con i vantaggi dell'implementazione eseguibile. Gli strumenti di sviluppo Microsoft Visual Studio facilitano la scrittura di server DLL, ma un server DLL presenta limiti. L'esecuzione del server DLL in un processo surrogato offre diversi vantaggi:

-   Isolamento degli errori e possibilità di gestire più client contemporaneamente.
-   In un ambiente distribuito è possibile usare un'implementazione del server DLL per la manutenzione di client remoti.
-   Potrebbe consentire ai client di proteggersi da codice server non attendibile, consentendo l'accesso ai servizi forniti dal server DLL.
-   L'esecuzione di un server DLL in un surrogato fornisce alla DLL la sicurezza del surrogato.

COM fornisce un processo surrogato predefinito oppure è possibile scrivere un surrogato personalizzato in caso di esigenze speciali.

Negli argomenti seguenti vengono fornite ulteriori informazioni sui surrogati dll:

-   [Requisiti del server DLL](dll-server-requirements.md)
-   [Uso del surrogato System-Supplied](using-the-system-supplied-surrogate.md)
-   [Scrittura di un surrogato personalizzato](writing-a-custom-surrogate.md)

 

 




