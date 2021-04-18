---
description: Nell'argomento seguente viene descritto come eseguire la riproduzione semplice.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Riproduzione semplice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318935"
---
# <a name="simple-playback"></a><span data-ttu-id="94169-103">Riproduzione semplice</span><span class="sxs-lookup"><span data-stu-id="94169-103">Simple Playback</span></span>

<span data-ttu-id="94169-104">Nell'argomento seguente viene descritto come eseguire la riproduzione semplice.</span><span class="sxs-lookup"><span data-stu-id="94169-104">The following topic describes how to perform simple playback.</span></span>

<span data-ttu-id="94169-105">**Per eseguire la riproduzione semplice**</span><span class="sxs-lookup"><span data-stu-id="94169-105">**To perform simple playback**</span></span>

1.  <span data-ttu-id="94169-106">Selezionare il terminale riproduzione file a livello di chiamata.</span><span class="sxs-lookup"><span data-stu-id="94169-106">Select the File Playback Terminal at the call level.</span></span>
2.  <span data-ttu-id="94169-107">Creare il terminale di riproduzione nella chiamata TAPI.</span><span class="sxs-lookup"><span data-stu-id="94169-107">Create the Playback Terminal on the TAPI call.</span></span>
3.  <span data-ttu-id="94169-108">Impostare le proprietà: nome file e tipo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="94169-108">Set properties—file name and type of storage.</span></span>
4.  <span data-ttu-id="94169-109">Chiamare il metodo [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sul terminale riproduzione file per avviare la riproduzione dei flussi.</span><span class="sxs-lookup"><span data-stu-id="94169-109">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of streams.</span></span>

<span data-ttu-id="94169-110">Il codice di esempio seguente illustra la riproduzione semplice.</span><span class="sxs-lookup"><span data-stu-id="94169-110">The following example code demonstrates simple playback.</span></span>

<span data-ttu-id="94169-111">Per prima cosa, usare l'interfaccia [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) per creare il terminale per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="94169-111">First, use the [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) interface to create the terminal for recording.</span></span> <span data-ttu-id="94169-112">Indica a TSP/MSP di eseguire la riproduzione dei file in questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="94169-112">This instructs the TSP/MSP to perform file playback on this call.</span></span> <span data-ttu-id="94169-113">Il TSP/MSP crea un terminale che l'applicazione deve usare e la restituisce in seguito al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="94169-113">The TSP/MSP creates a terminal for the application to use, and returns it on success.</span></span>


```C++

```



<span data-ttu-id="94169-114">Ottenere il puntatore all'interfaccia [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) dall'interfaccia terminal e usarlo per impostare il nome del file per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="94169-114">Get the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface pointer from the terminal interface and use it to set the file name to play back.</span></span>


```C++
pMediaPlayback->Release();
```



<span data-ttu-id="94169-115">Supponendo che il file contenga un flusso audio e che la chiamata disponga di un flusso audio di acquisizione, il contenuto audio nel file verrà riprodotto in quel flusso.</span><span class="sxs-lookup"><span data-stu-id="94169-115">Assuming that the file contains one audio stream, and the call has a capture audio stream, the audio content in the file will play back on that stream.</span></span>

 

 



