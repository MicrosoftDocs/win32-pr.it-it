---
title: Funzioni wrapper plug-in
description: Funzioni wrapper che consentono di chiamare una funzione pubblica su qualsiasi adattatore collegato alla pipeline senza acquisire manualmente un puntatore all'adattatore.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- Windows Api Biometric Framework Windows API Biometric Framework , funzioni wrapper plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b3f6991d0723f284bb95ecfd40d7931c48aa8647fb52e2b34a959791a7338b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101251"
---
# <a name="plug-in-wrapper-functions"></a>Funzioni wrapper plug-in

L Windows'API Biometric Framework include funzioni wrapper che consentono di chiamare una funzione pubblica su qualsiasi adattatore collegato alla pipeline senza acquisire manualmente un puntatore all'adapter. Ogni wrapper controlla gli argomenti di input, recupera un puntatore dell'adattatore e chiama la funzione richiesta. Ad esempio, il wrapper **WbioEngineSetHashAlgorithm** ha la firma seguente.


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



La funzione verifica che l'argomento *Pipeline* non sia **NULL,** che esista un adattatore motore e che la funzione [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) esista. Tutte le funzioni wrapper sono definite nel file di intestazione \_ adapter.h di Winbio. Negli argomenti seguenti vengono illustrati i wrapper disponibili.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                               | Descrizione                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Wrapper dell'adapter del motore](engine-adapter-wrappers.md)<br/>   | Funzioni che è possibile usare per chiamare funzioni nell'adattatore del motore. Queste funzioni sono definite in Winbio \_ adapter.h.<br/>  |
| [Wrapper dell'adattatore del sensore](sensor-adapter-wrappers.md)<br/>   | Funzioni che è possibile usare per chiamare funzioni sull'adattatore del sensore. Queste funzioni sono definite in Winbio \_ adapter.h.<br/>  |
| [Archiviazione Wrapper dell'adapter](storage-adapter-wrappers.md)<br/> | Funzioni che è possibile usare per chiamare funzioni nella scheda di archiviazione. Queste funzioni sono definite in Winbio \_ adapter.h.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul plug-in](plug-in-reference.md)
</dt> </dl>

 

 





