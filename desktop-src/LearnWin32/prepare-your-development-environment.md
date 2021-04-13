---
title: Preparare l'ambiente di sviluppo
description: Preparare l'ambiente di sviluppo
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337206"
---
# <a name="prepare-your-development-environment"></a><span data-ttu-id="6e725-103">Preparare l'ambiente di sviluppo</span><span class="sxs-lookup"><span data-stu-id="6e725-103">Prepare Your Development Environment</span></span>

<span data-ttu-id="6e725-104">Per scrivere un programma Windows in C o C++, è necessario installare Microsoft Windows Software Development Kit (SDK) o Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6e725-104">To write a Windows program in C or C++, you must install the Microsoft Windows Software Development Kit (SDK) or Microsoft Visual Studio.</span></span> <span data-ttu-id="6e725-105">Il Windows SDK contiene le intestazioni e le librerie necessarie per la compilazione e il collegamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e725-105">The Windows SDK contains the headers and libraries necessary to compile and link your application.</span></span> <span data-ttu-id="6e725-106">Il Windows SDK contiene anche gli strumenti da riga di comando per la compilazione di applicazioni Windows, tra cui il compilatore Visual C++ e il linker.</span><span class="sxs-lookup"><span data-stu-id="6e725-106">The Windows SDK also contains command-line tools for building Windows applications, including the Visual C++ compiler and linker.</span></span> <span data-ttu-id="6e725-107">Sebbene sia possibile compilare e compilare programmi Windows con gli strumenti da riga di comando, è consigliabile usare Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6e725-107">Although you can compile and build Windows programs with the command-line tools, we recommend using Microsoft Visual Studio.</span></span> <span data-ttu-id="6e725-108">È possibile scaricare gratuitamente una community di [Visual Studio o](https://visualstudio.microsoft.com/downloads/)versioni di valutazione gratuite di altre versioni di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6e725-108">You can download a free download of Visual Studio Community or free trials of other versions of Visual Studio [here](https://visualstudio.microsoft.com/downloads/).</span></span>

<span data-ttu-id="6e725-109">Ogni versione del Windows SDK è destinata alla versione più recente di Windows e a diverse versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="6e725-109">Each release of the Windows SDK targets the latest version of Windows as well as several previous versions.</span></span> <span data-ttu-id="6e725-110">Nelle note sulla versione sono elencate le piattaforme specifiche supportate, ma a meno che non si stia gestendo un'applicazione per una versione molto vecchia di Windows, è necessario installare la versione più recente del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6e725-110">The release notes list the specific platforms that are supported, but unless you are maintaining an application for a very old version of Windows, you should install the latest release of the Windows SDK.</span></span> <span data-ttu-id="6e725-111">È possibile scaricare la Windows SDK più recente [qui](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="6e725-111">You can download the latest Windows SDK [here](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="6e725-112">Il Windows SDK supporta lo sviluppo di applicazioni sia a 32 bit che a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6e725-112">The Windows SDK supports development of both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="6e725-113">Le API di Windows sono progettate in modo che lo stesso codice possa essere compilato per 32 bit o 64 bit senza apportare modifiche.</span><span class="sxs-lookup"><span data-stu-id="6e725-113">The Windows APIs are designed so that the same code can compile for 32-bit or 64-bit without changes.</span></span>

> [!Note]  
> <span data-ttu-id="6e725-114">Il Windows SDK non supporta lo sviluppo di driver hardware e in questa serie non verrà illustrato lo sviluppo di driver.</span><span class="sxs-lookup"><span data-stu-id="6e725-114">The Windows SDK does not support hardware driver development, and this series will not discuss driver development.</span></span> <span data-ttu-id="6e725-115">Per informazioni sulla scrittura di un driver hardware, vedere [Introduzione con i driver di Windows](/windows-hardware/drivers/gettingstarted/).</span><span class="sxs-lookup"><span data-stu-id="6e725-115">For information about writing a hardware driver, see [Getting Started with Windows Drivers](/windows-hardware/drivers/gettingstarted/).</span></span>

## <a name="next"></a><span data-ttu-id="6e725-116">Prossima</span><span class="sxs-lookup"><span data-stu-id="6e725-116">Next</span></span>

[<span data-ttu-id="6e725-117">Convenzioni di codifica Windows</span><span class="sxs-lookup"><span data-stu-id="6e725-117">Windows Coding Conventions</span></span>](windows-coding-conventions.md)

## <a name="related-topics"></a><span data-ttu-id="6e725-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e725-118">Related topics</span></span>

* [<span data-ttu-id="6e725-119">Download di Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6e725-119">Download Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="6e725-120">Scarica Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6e725-120">Download Windows SDK</span></span>](https://developer.microsoft.com/windows/downloads/windows-10-sdk)