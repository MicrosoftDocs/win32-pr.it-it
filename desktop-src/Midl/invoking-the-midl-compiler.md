---
title: Richiamo del compilatore MIDL
description: Il compilatore MIDL può generare codice per diverse piattaforme e versioni di sistema. Per ulteriori informazioni sulle opzioni suggerite e su come generare codice ottimizzato per una versione specifica, consultare l'opzione/target.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL compilatore MIDL, chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/15/2019
ms.locfileid: "106299007"
---
# <a name="invoking-the-midl-compiler"></a>Richiamo del compilatore MIDL

Il compilatore MIDL può generare codice per diverse piattaforme e versioni di sistema. Per ulteriori informazioni sulle opzioni suggerite e su come generare codice ottimizzato per una versione specifica, consultare l'opzione [**/target**](-target.md) .

Eseguire il compilatore MIDL dalla riga di comando usando il comando seguente:

 *<  opzioni >* MIDL **nomefile. idl**

dove *<  Options >* rappresenta le opzioni della riga di comando che si vuole usare e filename. idl è il nome del file MIDL da compilare.

Un elenco completo delle opzioni e dei commutatori del compilatore MIDL è disponibile quando si usa il compilatore MIDL [**/Help**](-help-.md) e/? interruttori. Le opzioni sono organizzate in base alle categorie. Per informazioni dettagliate, vedere la Guida di [riferimento a MIDL Command-Line](midl-command-line-reference.md).

> [!NOTE]
> Il nuovo flag globale **$ ( \_ ottimizzazione MIDL)** esiste in Win32. mak. Quando si compila un file con estensione IDL utilizzando questo flag, lo stub generato può utilizzare le funzionalità RPC più recenti disponibili sulla piattaforma specificata e potenzialmente migliorare le prestazioni e la stabilità dell'applicazione. È consigliabile che le applicazioni usino questo flag quando si usa MIDL.
>
> **MIDL** **$ ( \_ ottimizzazione MIDL)** **...**