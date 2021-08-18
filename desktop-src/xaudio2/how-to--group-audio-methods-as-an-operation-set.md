---
description: Questo argomento illustra come raggruppare i metodi XAudio2 in modo che siano effettive contemporaneamente.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Procedura: Raggruppare metodi audio come set di operazioni'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f5c1d27e33db4c0f7910761a7be574b72e9ac7aaa91b14329fa003792860d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082925"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a>Procedura: Raggruppare metodi audio come set di operazioni

Questo argomento illustra come raggruppare i metodi XAudio2 in modo che siano effettive contemporaneamente.

## <a name="to-group-audio-methods-as-an-operation-set"></a>Per raggruppare i metodi audio come set di operazioni

1.  Dichiarare un contatore del set di operazioni globale.

    Il [contatore del set](operation-sets.md) di operazioni garantisce che ogni set di operazioni sia univoco.

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  Incrementare il contatore globale.

    Ogni volta che si invia un nuovo [set di operazioni,](operation-sets.md)il contatore globale deve incrementare per garantire che ogni set sia univoco.

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  Raggruppare le chiamate al metodo impostando i parametri [del set di](operation-sets.md) operazioni.

4.  Impostare i [parametri del set](operation-sets.md) di operazioni sul valore corrente del contatore globale.

    In questo caso, quattro chiamate a [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) vengono raggruppate come un unico [set di operazioni.](operation-sets.md) Il raggruppamento delle chiamate fa sì che tutti e quattro i suoni inizino esattamente nello stesso momento.

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  Avviare il [set di operazioni](operation-sets.md).

    Dopo aver chiamato tutti i metodi nel set, avviare il set chiamando [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con il valore corrente del contatore globale.

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

 

 
