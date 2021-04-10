---
description: Le applicazioni possono produrre file minidump in modalità utente che contengono un subset utile delle informazioni contenute in un file di dump di arresto anomalo del sistema.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: File minidump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126060"
---
# <a name="minidump-files"></a>File minidump

Le applicazioni possono produrre file minidump in modalità utente che contengono un subset utile delle informazioni contenute in un file di dump di arresto anomalo del sistema. Le applicazioni possono creare file di minidump in modo molto rapido ed efficiente. Poiché i file di minidump sono di piccole dimensioni, possono essere facilmente inviati tramite Internet al supporto tecnico per l'applicazione.

Un file minidump non contiene quante più informazioni di un file di dump di arresto anomalo del sistema, ma contiene informazioni sufficienti per eseguire operazioni di debug di base. Per leggere un file di minidump, è necessario che i file binari e i file di simboli siano disponibili per il debugger.

Le versioni correnti di Microsoft Office e Microsoft Windows creano file di minidump allo scopo di analizzare gli errori nei computer dei clienti.

Con i file di minidump vengono usate le funzioni DbgHelp seguenti.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



