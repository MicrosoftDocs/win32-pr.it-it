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
# <a name="how-to-group-audio-methods-as-an-operation-set"></a>Procedura: Raggruppare metodi audio come set di operazioni

In questo argomento viene illustrato come raggruppare i metodi XAudio2 in modo che abbiano effetto allo stesso tempo.

## <a name="to-group-audio-methods-as-an-operation-set"></a>Per raggruppare i metodi audio come un set di operazioni

1.  Dichiarare un contatore del set di operazioni globale.

    Il contatore del [set di operazioni](operation-sets.md) garantisce che ogni set di operazioni sia univoco.

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  Incrementare il contatore globale.

    Ogni volta che si invia un nuovo [set di operazioni](operation-sets.md), il contatore globale deve incrementare per assicurarsi che ogni set sia univoco.

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  Raggruppare le chiamate al metodo impostando i parametri del [set di operazioni](operation-sets.md) .

4.  Impostare i parametri del [set di operazioni](operation-sets.md) sul valore corrente del contatore globale.

    In questo caso, le quattro chiamate a [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) vengono raggruppate come un unico [set di operazioni](operation-sets.md). Il raggruppamento delle chiamate comporta l'avvio di tutti e quattro i suoni esattamente allo stesso tempo.

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  Avviare il [set di operazioni](operation-sets.md).

    Dopo aver chiamato tutti i metodi del set, avviare il set chiamando [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con il valore corrente del contatore globale.

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di operazioni](operation-sets.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Set di operazioni XAudio2](xaudio2-operation-sets.md)
</dt> </dl>

 

 
