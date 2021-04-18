---
title: Apertura e chiusura di file
description: Apertura e chiusura di file
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen (funzione)
- AVIFileRelease (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321083"
---
# <a name="opening-and-closing-files"></a><span data-ttu-id="7e961-105">Apertura e chiusura di file</span><span class="sxs-lookup"><span data-stu-id="7e961-105">Opening and Closing Files</span></span>

<span data-ttu-id="7e961-106">Un'applicazione deve aprire un file AVI prima della lettura o della scrittura.</span><span class="sxs-lookup"><span data-stu-id="7e961-106">An application must open an AVI file before reading or writing.</span></span> <span data-ttu-id="7e961-107">Per aprire un file AVI, usare la funzione [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) .</span><span class="sxs-lookup"><span data-stu-id="7e961-107">To open an AVI file, use the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) function.</span></span> <span data-ttu-id="7e961-108">**AVIFileOpen** restituisce l'indirizzo di un'interfaccia file AVI contenente l'handle del file aperto e incrementa il conteggio dei riferimenti del file.</span><span class="sxs-lookup"><span data-stu-id="7e961-108">**AVIFileOpen** returns the address of an AVI file interface that contains the handle of the open file and increments the reference count of the file.</span></span>

<span data-ttu-id="7e961-109">La funzione **AVIFileOpen** supporta l'oggetto dei flag utilizzati con la funzione [OpenFile](/documentation/) .</span><span class="sxs-lookup"><span data-stu-id="7e961-109">The **AVIFileOpen** function supports the OF flags used with the [OpenFile](/documentation/) function.</span></span> <span data-ttu-id="7e961-110">Se un'applicazione scrive in un file esistente, deve includere il flag di \_ scrittura in **AVIFileOpen**.</span><span class="sxs-lookup"><span data-stu-id="7e961-110">If an application writes to an existing file, it must include the OF\_WRITE flag in **AVIFileOpen**.</span></span> <span data-ttu-id="7e961-111">Analogamente, se l'applicazione crea e scrive in un nuovo file, è necessario includere i \_ flag di creazione e di \_ scrittura in **AVIFileOpen**.</span><span class="sxs-lookup"><span data-stu-id="7e961-111">Similarly, if your application creates and writes to a new file, you must include the OF\_CREATE and OF\_WRITE flags in **AVIFileOpen**.</span></span>

<span data-ttu-id="7e961-112">Quando si apre un file con **AVIFileOpen**, è possibile usare un gestore di file predefinito oppure specificare un gestore di file personalizzato per la lettura e la scrittura nel file e nei relativi flussi di dati.</span><span class="sxs-lookup"><span data-stu-id="7e961-112">When you open a file using **AVIFileOpen**, you can use a default file handler or you can specify a custom file handler to read and write to the file and its data streams.</span></span> <span data-ttu-id="7e961-113">In entrambi i casi, AVIFile Cerca nel registro di sistema il gestore di file corretto da usare.</span><span class="sxs-lookup"><span data-stu-id="7e961-113">In either case, AVIFile searches the registry for the correct file handler to use.</span></span> <span data-ttu-id="7e961-114">È necessario assicurarsi che i gestori di file personalizzati si trovino nel registro di sistema prima che un'applicazione possa accedervi.</span><span class="sxs-lookup"><span data-stu-id="7e961-114">You must ensure custom file handlers are in the registry before an application can access them.</span></span>

<span data-ttu-id="7e961-115">È possibile incrementare il conteggio dei riferimenti di un file tramite la funzione [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) .</span><span class="sxs-lookup"><span data-stu-id="7e961-115">You can increment the reference count of a file by using the [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) function.</span></span> <span data-ttu-id="7e961-116">Ad esempio, è possibile eseguire questa operazione quando si passa un handle dell'interfaccia file a un'altra applicazione o quando si vuole lasciare un file aperto quando si usa una funzione che normalmente chiude il file.</span><span class="sxs-lookup"><span data-stu-id="7e961-116">For example, you might want to do this when passing a handle of the file interface to another application, or when you want to keep a file open while using a function that would normally close the file.</span></span>

<span data-ttu-id="7e961-117">È possibile chiudere un file usando la funzione [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .</span><span class="sxs-lookup"><span data-stu-id="7e961-117">You can close a file by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span> <span data-ttu-id="7e961-118">La funzione **AVIFileRelease** decrementa il conteggio dei riferimenti di un file AVI, Salva le modifiche apportate al file e quando il conteggio dei riferimenti raggiunge zero, chiude il file.</span><span class="sxs-lookup"><span data-stu-id="7e961-118">The **AVIFileRelease** function decrements the reference count of an AVI file, saves changes made to the file, and when the reference count reaches zero, closes the file.</span></span> <span data-ttu-id="7e961-119">Le applicazioni devono bilanciare il conteggio dei riferimenti includendo una chiamata a **AVIFileRelease** per ogni uso di [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) e **AVIFileAddRef**.</span><span class="sxs-lookup"><span data-stu-id="7e961-119">Your applications should balance the reference count by including a call to **AVIFileRelease** for each use of [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileAddRef**.</span></span>

> [!Note]  
> <span data-ttu-id="7e961-120">Un'applicazione può aprire un file con uno o più thread di programma.</span><span class="sxs-lookup"><span data-stu-id="7e961-120">An application can open a file with one or more program threads.</span></span> <span data-ttu-id="7e961-121">Tuttavia, per ottenere le migliori prestazioni possibili, solo un thread deve accedere al file in un momento qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="7e961-121">However, for the best possible performance, only one thread should access the file at any one time.</span></span>

 

 

 