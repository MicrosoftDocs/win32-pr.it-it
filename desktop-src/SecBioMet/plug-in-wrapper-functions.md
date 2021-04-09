---
title: Funzioni wrapper plug-in
description: Funzioni wrapper che consentono di chiamare una funzione pubblica su qualsiasi Adapter collegato alla pipeline senza acquisire manualmente un puntatore all'adapter.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- API Windows Biometric Framework API di Windows Biometric Framework, funzioni wrapper per il plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856710"
---
# <a name="plug-in-wrapper-functions"></a>Funzioni wrapper plug-in

L'API Windows Biometric Framework include funzioni wrapper che consentono di chiamare una funzione pubblica su qualsiasi Adapter collegato alla pipeline senza acquisire manualmente un puntatore alla scheda. Ogni wrapper controlla gli argomenti di input, recupera un puntatore di adapter e chiama la funzione richiesta. Il wrapper **WbioEngineSetHashAlgorithm** , ad esempio, ha la firma seguente:


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



La funzione verifica che l'argomento della *pipeline* non sia **null**, che esista un adattatore del motore e che la funzione [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) esista. Tutte le funzioni wrapper sono definite nel \_ file di intestazione WinBio adapter. h. Negli argomenti seguenti vengono illustrati i wrapper disponibili.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                               | Descrizione                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Wrapper dell'adattatore del motore](engine-adapter-wrappers.md)<br/>   | Funzioni che è possibile utilizzare per chiamare funzioni sull'adattatore del motore. Queste funzioni sono definite in WinBio \_ Adapter. h.<br/>  |
| [Wrapper adattatore sensore](sensor-adapter-wrappers.md)<br/>   | Funzioni che è possibile utilizzare per chiamare funzioni sulla scheda del sensore. Queste funzioni sono definite in WinBio \_ Adapter. h.<br/>  |
| [Wrapper dell'adattatore di archiviazione](storage-adapter-wrappers.md)<br/> | Funzioni che è possibile utilizzare per chiamare funzioni sull'adattatore di archiviazione. Queste funzioni sono definite in WinBio \_ Adapter. h.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al plug-in](plug-in-reference.md)
</dt> </dl>

 

 





