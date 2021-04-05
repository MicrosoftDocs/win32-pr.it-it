---
description: In questo argomento viene illustrato come raggruppare i metodi XAudio2 in modo che abbiano effetto allo stesso tempo.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Procedura: Raggruppare metodi audio come set di operazioni'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883129"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="5e5ea-103">Procedura: Raggruppare metodi audio come set di operazioni</span><span class="sxs-lookup"><span data-stu-id="5e5ea-103">How to: Group Audio Methods as an Operation Set</span></span>

<span data-ttu-id="5e5ea-104">In questo argomento viene illustrato come raggruppare i metodi XAudio2 in modo che abbiano effetto allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="5e5ea-104">This topic shows you how you can group together XAudio2 methods so they take effect at the same time.</span></span>

## <a name="to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="5e5ea-105">Per raggruppare i metodi audio come un set di operazioni</span><span class="sxs-lookup"><span data-stu-id="5e5ea-105">To group audio methods as an operation set</span></span>

1.  <span data-ttu-id="5e5ea-106">Dichiarare un contatore del set di operazioni globale.</span><span class="sxs-lookup"><span data-stu-id="5e5ea-106">Declare a global operation set counter.</span></span>

    <span data-ttu-id="5e5ea-107">Il contatore del [set di operazioni](operation-sets.md) garantisce che ogni set di operazioni sia univoco.</span><span class="sxs-lookup"><span data-stu-id="5e5ea-107">The [operation set](operation-sets.md) counter ensures that each operation set is unique.</span></span>

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  <span data-ttu-id="5e5ea-108">Incrementare il contatore globale.</span><span class="sxs-lookup"><span data-stu-id="5e5ea-108">Increment the global counter.</span></span>

    <span data-ttu-id="5e5ea-109">Ogni volta che si invia un nuovo [set di operazioni](operation-sets.md), il contatore globale deve incrementare per assicurarsi che ogni set sia univoco.</span><span class="sxs-lookup"><span data-stu-id="5e5ea-109">Each time you submit a new [operation set](operation-sets.md), the global counter should increment to ensure each set is unique.</span></span>

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  <span data-ttu-id="5e5ea-110">Raggruppare le chiamate al metodo impostando i parametri del [set di operazioni](operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="5e5ea-110">Group the method calls by setting their [operation set](operation-sets.md) parameters.</span></span>

4.  <span data-ttu-id="5e5ea-111">Impostare i parametri del [set di operazioni](operation-sets.md) sul valore corrente del contatore globale.</span><span class="sxs-lookup"><span data-stu-id="5e5ea-111">Set the [operation set](operation-sets.md) parameters to the current value of the global counter.</span></span>

    <span data-ttu-id="5e5ea-112">In questo caso, le quattro chiamate a [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) vengono raggruppate come un unico [set di operazioni](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="5e5ea-112">In this case, four calls to [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) are grouped as one [operation set](operation-sets.md).</span></span> <span data-ttu-id="5e5ea-113">Il raggruppamento delle chiamate comporta l'avvio di tutti e quattro i suoni esattamente allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="5e5ea-113">Grouping the calls causes all four of the sounds to start at exactly the same time.</span></span>

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  <span data-ttu-id="5e5ea-114">Avviare il [set di operazioni](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="5e5ea-114">Start the [operation set](operation-sets.md).</span></span>

    <span data-ttu-id="5e5ea-115">Dopo aver chiamato tutti i metodi del set, avviare il set chiamando [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con il valore corrente del contatore globale.</span><span class="sxs-lookup"><span data-stu-id="5e5ea-115">After you call all the methods in the set, start the set by calling [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the current value of the global counter.</span></span>

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5e5ea-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e5ea-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e5ea-117">Set di operazioni</span><span class="sxs-lookup"><span data-stu-id="5e5ea-117">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="5e5ea-118">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="5e5ea-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="5e5ea-119">Set di operazioni XAudio2</span><span class="sxs-lookup"><span data-stu-id="5e5ea-119">XAudio2 Operation Sets</span></span>](xaudio2-operation-sets.md)
</dt> </dl>

 

 
