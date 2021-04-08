---
description: In questo argomento viene illustrato come stampare da un programma Windows nativo utilizzando GDI&\# 160; Stampa&\# 160; API.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: "Procedura: stampare con l'API di stampa GDI"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885178"
---
# <a name="how-to-print-using-the-gdi-print-api"></a><span data-ttu-id="84b22-103">Procedura: stampare con l'API di stampa GDI</span><span class="sxs-lookup"><span data-stu-id="84b22-103">How To: Print Using the GDI Print API</span></span>

<span data-ttu-id="84b22-104">In questo argomento viene illustrato come stampare da un programma Windows nativo utilizzando l' [API di stampa GDI](gdi-printing.md).</span><span class="sxs-lookup"><span data-stu-id="84b22-104">This topic introduces how to print from a native Windows program using the [GDI Print API](gdi-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="84b22-105">Panoramica</span><span class="sxs-lookup"><span data-stu-id="84b22-105">Overview</span></span>

<span data-ttu-id="84b22-106">La stampa è in genere parte integrante di un programma Windows nativo, pertanto non è una funzionalità che è possibile aggiungere facilmente dopo aver scritto il programma.</span><span class="sxs-lookup"><span data-stu-id="84b22-106">Printing is usually an integral part of a native Windows program, so it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="84b22-107">Quando si progetta un programma per Windows 7, è consigliabile utilizzare l' [API di stampa XPS](xps-printing.md) per fornire la funzionalità di stampa perché fornisce la compatibilità per il futuro.</span><span class="sxs-lookup"><span data-stu-id="84b22-107">When designing a program for Windows 7, you should consider using the [XPS Print API](xps-printing.md) to provide the printing functionality because it provides the most compatibility for the future.</span></span> <span data-ttu-id="84b22-108">I programmi che devono essere eseguiti in Windows Vista e nelle versioni precedenti di Windows utilizzeranno con maggiore probabilità l' [API di stampa GDI](gdi-printing.md) per fornire funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="84b22-108">Programs that must run on Windows Vista and earlier versions of Windows will most likely use the [GDI Print API](gdi-printing.md) to provide printing functionality.</span></span> <span data-ttu-id="84b22-109">L'API di stampa GDI è supportata anche in Windows 7, ma è più limitata rispetto all'API di stampa XPS.</span><span class="sxs-lookup"><span data-stu-id="84b22-109">The GDI Print API is also supported in Windows 7, but it is more limited than the XPS Print API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84b22-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84b22-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84b22-111">Uso della stampa</span><span class="sxs-lookup"><span data-stu-id="84b22-111">Using Printing</span></span>](using-printing.md)
</dt> <dt>

[<span data-ttu-id="84b22-112">Come stampare da un'applicazione Windows</span><span class="sxs-lookup"><span data-stu-id="84b22-112">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



