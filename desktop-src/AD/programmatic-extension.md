---
title: Estensione a livello di codice
description: Le estensioni a livello di codice hanno tuttavia diversi vantaggi, ma un'applicazione è opaca. l'amministratore deve considerare attendibile la documentazione inclusa nell'applicazione di installazione.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Estensione a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc8f049eb243dea0bfb8ad1eef4754d3713b9e908a16837abb832bab829b7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025469"
---
# <a name="programmatic-extension"></a>Estensione a livello di codice

Il vantaggio di un file LDIF è che l'amministratore può esaminarne la funzione. Tuttavia, lo schema può essere esteso anche a livello di codice. Le estensioni a livello di codice hanno diversi vantaggi, ma un'applicazione è opaca. l'amministratore deve considerare attendibile la documentazione inclusa nell'applicazione di installazione. L'uso di estensioni dello schema a livello di codice può essere una barriera alla distribuzione per le applicazioni che le usano. Un'estensione a livello di codice è invariante. si tratta di un Windows NT eseguibile. Il file binario non può essere manomesso, a differenza di un file LDIF o .csv, che può essere modificato inavvertitamente o in modo dannoso.

I vantaggi di un file LDIF includono:

-   Le applicazioni possono rilevare e ripristinare gli errori e fornire commenti e suggerimenti agli utenti.
-   Le applicazioni possono gestire Unicode senza ricorrere alla codifica Base64.
-   Le applicazioni possono sfruttare Windows api di configurazione del programma di installazione.
-   Le applicazioni possono essere firmate per stabilire l'autenticità.

 

 




