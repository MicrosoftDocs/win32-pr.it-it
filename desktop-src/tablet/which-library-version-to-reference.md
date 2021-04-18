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
# <a name="which-library-version-to-reference"></a><span data-ttu-id="20b56-103">Versione della libreria a cui fare riferimento</span><span class="sxs-lookup"><span data-stu-id="20b56-103">Which Library Version to Reference</span></span>

<span data-ttu-id="20b56-104">In questo argomento vengono descritte le differenze tra le versioni binarie della libreria Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="20b56-104">This topic describes the differences between the Tablet PC library binary versions.</span></span>

## <a name="tablet-pc-library-versions"></a><span data-ttu-id="20b56-105">Versioni della libreria di Tablet PC</span><span class="sxs-lookup"><span data-stu-id="20b56-105">Tablet PC Library Versions</span></span>

<span data-ttu-id="20b56-106">I file binari della libreria Tablet PC (Microsoft.Ink.dll) sono stati aggiornati in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20b56-106">The Tablet PC library binaries (Microsoft.Ink.dll) have been updated in Windows Vista.</span></span> <span data-ttu-id="20b56-107">Questi file binari sono detti "versione 6,0" per la co-incide con la versione di Windows in cui vengono rilasciati.</span><span class="sxs-lookup"><span data-stu-id="20b56-107">Theses binaries are referred to as "version 6.0" to co-incide with the version of Windows in which they are being released.</span></span>

<span data-ttu-id="20b56-108">La versione più recente dei file binari compatibili con Windows XP è detta "versione 1,7".</span><span class="sxs-lookup"><span data-stu-id="20b56-108">The most recent release of the binaries that are compatible with Windows XP is referred to as "version 1.7".</span></span>

<span data-ttu-id="20b56-109">Il Windows SDK può essere installato nei computer con vista e XP e il Windows SDK include entrambe le versioni di Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="20b56-109">The Windows SDK can be installed on both Vista and XP machines, and the Windows SDK includes both versions of Microsoft.Ink.dll.</span></span>

<span data-ttu-id="20b56-110">Sono installati in:</span><span class="sxs-lookup"><span data-stu-id="20b56-110">These are installed in:</span></span>

1. <span data-ttu-id="20b56-111">% programmi% \\ assembly di riferimento \\ Microsoft \\ Tablet \\ PC v 1.7 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="20b56-111">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v1.7\\Microsoft.Ink.dll</span></span>

2. <span data-ttu-id="20b56-112">% programmi% \\ assembly di riferimento \\ Microsoft \\ Tablet \\ PC v 6.0 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="20b56-112">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v6.0\\Microsoft.Ink.dll</span></span>

<span data-ttu-id="20b56-113">I file binari della versione 6,0 sono compatibili solo con Windows Vista e le applicazioni scritte su di essi devono essere eseguite solo in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20b56-113">The version 6.0 binaries are only compatible with Windows Vista, and applications written against them should only ever be run on Windows Vista.</span></span>

<span data-ttu-id="20b56-114">Un'applicazione scritta con i file binari della versione 1,7 dovrebbe essere eseguita senza modifiche se installata in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20b56-114">An application written against the version 1.7 binaries should run without modification when installed on Windows Vista.</span></span>

 

 



