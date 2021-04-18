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
# <a name="gpu-accelerated-ml-training"></a>Training di Machine Learning con accelerazione GPU

![Immagine di Windows Machine Learning](images/winml-graphic.png)

Questa documentazione illustra gli elementi attualmente supportati dall'anteprima di training di Machine Learning (ML) GPU accelerata per il [sottosistema Windows per Linux](/windows/wsl/about) (WSL) e le finestre native.  

Questa versione di anteprima supporta scenari professionali e principianti. Di seguito sono riportati i puntatori alle guide dettagliate su come ottenere la configurazione del sistema in base al livello di esperienza in ML, al fornitore della GPU e alla raccolta software che si intende usare. 

> [!NOTE]
> Le funzionalità seguenti sono disponibili in anteprima e sono soggette a modifiche.


## <a name="professionals"></a>Professionisti

Per gli esperti di dati professionali che usano quotidianamente un ambiente Linux nativo per lo sviluppo e la sperimentazione di machine learning a ciclo interno e una GPU NVIDIA, è consigliabile configurare l' [Anteprima di NVIDIA CUDA in WSL 2.](gpu-cuda-in-wsl.md)

## <a name="students-and-beginners"></a>Studenti e principianti 

Per gli studenti o i principianti che vogliono iniziare a sviluppare le proprie conoscenze nello spazio ML, è consigliabile configurare TensorFlow con il pacchetto back-end DirectML. Questo pacchetto accelera attualmente i flussi di lavoro sulle GPU AMD e Intel. Il supporto per le GPU NVIDIA sarà presto disponibile. 

Per coloro che hanno familiarità con un ambiente Linux nativo che iniziano a usare i flussi di lavoro di ML, è consigliabile eseguire il [pacchetto TensorFlow con DirectML in WSL 2](gpu-tensorflow-wsl.md). 

Per coloro che hanno familiarità con Windows che iniziano a usare i flussi di lavoro di ML, è consigliabile configurare il [pacchetto TensorFlow con DirectML nelle finestre native](gpu-tensorflow-windows.md). 

## <a name="next-steps"></a>Passaggi successivi

* [Abilitare la versione di anteprima di NVIDIA CUDA in WSL 2](gpu-cuda-in-wsl.md).
* [Abilitare TensorFlow con il pacchetto DirectML all'interno di WSL 2](gpu-tensorflow-wsl.md).
* [Abilitare TensorFlow con il pacchetto DirectML nelle finestre native](gpu-tensorflow-windows.md).