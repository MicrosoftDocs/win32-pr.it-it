---
title: Estensione a livello di codice
description: Le estensioni programmatiche presentano diversi meriti, tuttavia un'applicazione è opaca; l'amministratore deve considerare attendibile la documentazione inclusa nell'applicazione di installazione.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Estensione a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707582"
---
# <a name="programmatic-extension"></a>Estensione a livello di codice

Il vantaggio di un file LDIF è che l'amministratore può esaminarne la funzione. Tuttavia, lo schema può anche essere esteso a livello di codice. Le estensioni a livello di codice hanno diversi meriti, ma un'applicazione è opaca; l'amministratore deve considerare attendibile la documentazione inclusa nell'applicazione di installazione. L'utilizzo delle estensioni dello schema programmatico può essere una barriera alla distribuzione per le applicazioni che le utilizzano. Un'estensione a livello di codice è invariante. si tratta di un eseguibile di Windows NT. Il file binario non può essere alterato, a differenza di un file LDIF o CSV, che può essere modificato inavvertitamente o intenzionalmente.

I vantaggi di un file LDIF includono:

-   Le applicazioni possono rilevare e correggere gli errori e fornire commenti e suggerimenti degli utenti.
-   Le applicazioni possono gestire Unicode senza ricorrere alla codifica Base64.
-   Le applicazioni possono utilizzare le API di installazione Windows Installer.
-   Le applicazioni possono essere firmate per stabilire l'autenticità.

 

 




