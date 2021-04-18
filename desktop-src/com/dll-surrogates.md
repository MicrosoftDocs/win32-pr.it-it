---
title: Surrogati DLL
description: Surrogati DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298938"
---
# <a name="dll-surrogates"></a>Surrogati DLL

COM rende possibile la creazione di server DLL che possono essere caricati in un processo EXE surrogato. Questa operazione combina la facilità di scrittura dei server DLL con i vantaggi dell'implementazione eseguibile. Gli strumenti di sviluppo come Microsoft Visual Studio facilitano la scrittura dei server DLL, ma un server DLL ha limiti. L'esecuzione del server DLL in un processo surrogato offre diversi vantaggi:

-   Isolamento degli errori e possibilità di servire contemporaneamente più client.
-   In un ambiente distribuito, è possibile usare un'implementazione del server DLL per servire i client remoti.
-   Potrebbe consentire ai client di proteggersi da codice server non attendibile consentendo loro di accedere ai servizi forniti dal server DLL.
-   L'esecuzione di un server DLL in un surrogato fornisce la DLL con la sicurezza del surrogato.

COM fornisce un processo surrogato predefinito oppure è possibile scrivere un surrogato personalizzato se si hanno esigenze particolari.

Negli argomenti seguenti vengono fornite ulteriori informazioni sui surrogati della DLL:

-   [Requisiti del server DLL](dll-server-requirements.md)
-   [Uso del surrogato System-Supplied](using-the-system-supplied-surrogate.md)
-   [Scrittura di un surrogato personalizzato](writing-a-custom-surrogate.md)

 

 




