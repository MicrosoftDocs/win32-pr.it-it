---
description: Le applicazioni possono produrre file di minidump in modalità utente, che contengono un utile subset delle informazioni contenute in un file di dump di arresto anomalo del sistema.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: File di minidump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412e719d54f34c9766981667be35990c37ae3511eaecc8836ceac0311a5105e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406091"
---
# <a name="minidump-files"></a>File di minidump

Le applicazioni possono produrre file di minidump in modalità utente, che contengono un utile subset delle informazioni contenute in un file di dump di arresto anomalo del sistema. Le applicazioni possono creare file di minidump in modo molto rapido ed efficiente. Poiché i file di minidump sono di piccole dimensioni, possono essere facilmente inviati tramite Internet al supporto tecnico per l'applicazione.

Un file di minidump non contiene tutte le informazioni di un file di dump completo dell'arresto anomalo del sistema, ma contiene informazioni sufficienti per eseguire operazioni di debug di base. Per leggere un file di minidump, è necessario disporre dei file binari e dei file di simboli disponibili per il debugger.

Le versioni correnti Microsoft Office e Microsoft Windows creare file di minidump allo scopo di analizzare gli errori nei computer dei clienti.

Le funzioni DbgHelp seguenti vengono usate con i file minidump.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



