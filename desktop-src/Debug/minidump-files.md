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
# <a name="minidump-files"></a><span data-ttu-id="2a9e5-103">File minidump</span><span class="sxs-lookup"><span data-stu-id="2a9e5-103">Minidump Files</span></span>

<span data-ttu-id="2a9e5-104">Le applicazioni possono produrre file minidump in modalità utente che contengono un subset utile delle informazioni contenute in un file di dump di arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="2a9e5-104">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="2a9e5-105">Le applicazioni possono creare file di minidump in modo molto rapido ed efficiente.</span><span class="sxs-lookup"><span data-stu-id="2a9e5-105">Applications can create minidump files very quickly and efficiently.</span></span> <span data-ttu-id="2a9e5-106">Poiché i file di minidump sono di piccole dimensioni, possono essere facilmente inviati tramite Internet al supporto tecnico per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a9e5-106">Because minidump files are small, they can be easily sent over the internet to technical support for the application.</span></span>

<span data-ttu-id="2a9e5-107">Un file minidump non contiene quante più informazioni di un file di dump di arresto anomalo del sistema, ma contiene informazioni sufficienti per eseguire operazioni di debug di base.</span><span class="sxs-lookup"><span data-stu-id="2a9e5-107">A minidump file does not contain as much information as a full crash dump file, but it contains enough information to perform basic debugging operations.</span></span> <span data-ttu-id="2a9e5-108">Per leggere un file di minidump, è necessario che i file binari e i file di simboli siano disponibili per il debugger.</span><span class="sxs-lookup"><span data-stu-id="2a9e5-108">To read a minidump file, you must have the binaries and symbol files available for the debugger.</span></span>

<span data-ttu-id="2a9e5-109">Le versioni correnti di Microsoft Office e Microsoft Windows creano file di minidump allo scopo di analizzare gli errori nei computer dei clienti.</span><span class="sxs-lookup"><span data-stu-id="2a9e5-109">Current versions of Microsoft Office and Microsoft Windows create minidump files for the purpose of analyzing failures on customers' computers.</span></span>

<span data-ttu-id="2a9e5-110">Con i file di minidump vengono usate le funzioni DbgHelp seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a9e5-110">The following DbgHelp functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="2a9e5-111">**MiniDumpCallback**</span><span class="sxs-lookup"><span data-stu-id="2a9e5-111">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="2a9e5-112">**MiniDumpReadDumpStream**</span><span class="sxs-lookup"><span data-stu-id="2a9e5-112">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="2a9e5-113">**MiniDumpWriteDump**</span><span class="sxs-lookup"><span data-stu-id="2a9e5-113">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



