---
title: Accelerazione GPU in WSL
description: Direct Machine Learning (DirectML) Powers GPU-accelerazione nel sottosistema Windows per Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 217a1763c0030a856e10a822cbd9f2642480c056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300378"
---
# <a name="gpu-accelerated-ml-training"></a><span data-ttu-id="fa008-103">Training di Machine Learning con accelerazione GPU</span><span class="sxs-lookup"><span data-stu-id="fa008-103">GPU accelerated ML training</span></span>

![Immagine di Windows Machine Learning](images/winml-graphic.png)

<span data-ttu-id="fa008-105">Questa documentazione illustra gli elementi attualmente supportati dall'anteprima di training di Machine Learning (ML) GPU accelerata per il [sottosistema Windows per Linux](/windows/wsl/about) (WSL) e le finestre native.</span><span class="sxs-lookup"><span data-stu-id="fa008-105">This documentation covers what is currently supported by the GPU accelerated machine learning (ML) training preview for the [Windows Subsystem for Linux](/windows/wsl/about) (WSL) and native Windows.</span></span>  

<span data-ttu-id="fa008-106">Questa versione di anteprima supporta scenari professionali e principianti.</span><span class="sxs-lookup"><span data-stu-id="fa008-106">This preview supports both professional and beginner scenarios.</span></span> <span data-ttu-id="fa008-107">Di seguito sono riportati i puntatori alle guide dettagliate su come ottenere la configurazione del sistema in base al livello di esperienza in ML, al fornitore della GPU e alla raccolta software che si intende usare.</span><span class="sxs-lookup"><span data-stu-id="fa008-107">Below you will find pointers to step-by-step guides on how to get your system setup depending on your level of expertise in ML, GPU vendor, and the software library you intend to use.</span></span> 

> [!NOTE]
> <span data-ttu-id="fa008-108">Le funzionalità seguenti sono disponibili in anteprima e sono soggette a modifiche.</span><span class="sxs-lookup"><span data-stu-id="fa008-108">The following features are in preview, and are subject to change.</span></span>


## <a name="professionals"></a><span data-ttu-id="fa008-109">Professionisti</span><span class="sxs-lookup"><span data-stu-id="fa008-109">Professionals</span></span>

<span data-ttu-id="fa008-110">Per gli esperti di dati professionali che usano quotidianamente un ambiente Linux nativo per lo sviluppo e la sperimentazione di machine learning a ciclo interno e una GPU NVIDIA, è consigliabile configurare l' [Anteprima di NVIDIA CUDA in WSL 2.](gpu-cuda-in-wsl.md)</span><span class="sxs-lookup"><span data-stu-id="fa008-110">If you’re a professional data scientist that uses a native Linux environment day-to-day for inner-loop ML development and experimentation, and you have an NVIDIA GPU, we recommend setting up the [NVIDIA CUDA preview in WSL 2.](gpu-cuda-in-wsl.md)</span></span>

## <a name="students-and-beginners"></a><span data-ttu-id="fa008-111">Studenti e principianti</span><span class="sxs-lookup"><span data-stu-id="fa008-111">Students and beginners</span></span> 

<span data-ttu-id="fa008-112">Per gli studenti o i principianti che vogliono iniziare a sviluppare le proprie conoscenze nello spazio ML, è consigliabile configurare TensorFlow con il pacchetto back-end DirectML.</span><span class="sxs-lookup"><span data-stu-id="fa008-112">If you’re a student or beginner looking to start building your knowledge in the ML space, we recommend setting up the TensorFlow with DirectML backend package.</span></span> <span data-ttu-id="fa008-113">Questo pacchetto accelera attualmente i flussi di lavoro sulle GPU AMD e Intel.</span><span class="sxs-lookup"><span data-stu-id="fa008-113">This package currently accelerates workflows on AMD and Intel GPUs.</span></span> <span data-ttu-id="fa008-114">Il supporto per le GPU NVIDIA sarà presto disponibile.</span><span class="sxs-lookup"><span data-stu-id="fa008-114">Support for NVIDIA GPUs is coming soon.</span></span> 

<span data-ttu-id="fa008-115">Per coloro che hanno familiarità con un ambiente Linux nativo che iniziano a usare i flussi di lavoro di ML, è consigliabile eseguire il [pacchetto TensorFlow con DirectML in WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="fa008-115">For those more familiar with a native Linux environment that are getting started with ML workflows, we recommend running the [TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span> 

<span data-ttu-id="fa008-116">Per coloro che hanno familiarità con Windows che iniziano a usare i flussi di lavoro di ML, è consigliabile configurare il [pacchetto TensorFlow con DirectML nelle finestre native](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="fa008-116">For those more familiar with Windows that are getting started with ML workflows, we recommend setting up the [TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="fa008-117">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="fa008-117">Next steps</span></span>

* <span data-ttu-id="fa008-118">[Abilitare la versione di anteprima di NVIDIA CUDA in WSL 2](gpu-cuda-in-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="fa008-118">[Enable NVIDIA CUDA preview in WSL 2](gpu-cuda-in-wsl.md).</span></span>
* <span data-ttu-id="fa008-119">[Abilitare TensorFlow con il pacchetto DirectML all'interno di WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="fa008-119">[Enable TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span>
* <span data-ttu-id="fa008-120">[Abilitare TensorFlow con il pacchetto DirectML nelle finestre native](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="fa008-120">[Enable TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span>