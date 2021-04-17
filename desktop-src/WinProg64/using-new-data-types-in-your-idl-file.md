---
title: Uso di nuovi tipi di dati nel file IDL
description: Il file di intestazione Basetsd. h definisce i nuovi tipi di dati necessari per la scrittura di applicazioni eseguite in Windows 32 e 64 bit.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- File di intestazione Basetsd. h a 64 bit programmazione Windows
- tipi di dati nel file IDL programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299978"
---
# <a name="using-new-data-types-in-your-idl-file"></a><span data-ttu-id="13665-105">Uso di nuovi tipi di dati nel file IDL</span><span class="sxs-lookup"><span data-stu-id="13665-105">Using New Data Types in Your IDL File</span></span>

<span data-ttu-id="13665-106">Il file di intestazione Basetsd. h definisce i nuovi tipi di dati necessari per la scrittura di applicazioni eseguite in Windows 32 e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="13665-106">The Basetsd.h header file defines the new data types needed for writing applications that run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="13665-107">Per utilizzare questi tipi di dati nelle interfacce, importare Basetsd. h nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="13665-107">To use these data types in your interfaces, import Basetsd.h into your IDL file.</span></span> <span data-ttu-id="13665-108">Non \# includere il file o si otterranno più definizioni in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="13665-108">Do not \#include the file or you will end up with multiple definitions at compile time.</span></span>

<span data-ttu-id="13665-109">In alternativa, è possibile includere o importare il file Basetsd. idl nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="13665-109">Alternatively, you can include or import the Basetsd.idl file into your IDL file.</span></span>

<span data-ttu-id="13665-110">Per ulteriori informazioni sull'aggiunta di file di intestazione di sistema al file IDL, vedere [importazione di file e librerie dei tipi](/windows/desktop/Midl/importing-files-and-type-libraries) e [importazione di file di intestazione di sistema](/windows/desktop/Midl/importing-system-header-files).</span><span class="sxs-lookup"><span data-stu-id="13665-110">For more information on adding system header files to your IDL file, see [Importing Files and Type Libraries](/windows/desktop/Midl/importing-files-and-type-libraries) and [Importing System Header Files](/windows/desktop/Midl/importing-system-header-files).</span></span>

 

 