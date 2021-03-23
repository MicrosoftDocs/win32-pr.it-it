---
title: Barriere UAV e barriere sullo stato delle risorse in DirectML
description: Vengono descritti i vantaggi di correttezza delle barriere e il modo in cui è possibile utilizzarli in DirectML.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 9bfc93d4fb28cff5d7d196287c6573e3e494d1d5
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548831"
---
# <a name="uav-barriers-and-resource-state-barriers-in-directml"></a>Barriere UAV e barriere sullo stato delle risorse in DirectML

## <a name="unordered-access-view-uav-barrier-requirements"></a>Requisiti della barriera Unordered Access View (UAV)

### <a name="uav-barriers-in-direct3d-12"></a>Barriere UAV in Direct3D 12

In Direct3D 12, il compute shader adiacente viene inviato all'interno dello stesso elenco di comandi per l'esecuzione in parallelo sulla GPU, a meno che non siano sincronizzati con una barriera di visualizzazione accesso non ordinato (UAV). Questo può migliorare le prestazioni aumentando l'utilizzo dell'hardware della GPU. Tuttavia, per impostazione predefinita, senza l'uso di una barriera UAV, l'esecuzione parallela di due invii adiacenti può causare un race condition se esiste una dipendenza dei dati tra i due invii; in alternativa, se entrambi gli invii eseguono Scritture UAV nelle stesse aree di memoria.

Una barriera UAV impone a tutti gli invii inviati in precedenza di completare esecuzione sulla GPU prima che possano iniziare le successive invii. Le barriere UAV vengono usate per sincronizzare gli invii nello stesso elenco di comandi per evitare le gare di dati. È possibile rilasciare una barriera UAV usando il metodo [ **ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

### <a name="uav-barriers-in-directml"></a>Barriere UAV in DirectML

In DirectML gli operatori vengono inviati in modo analogo al modo in cui i compute shader vengono inviati in Direct3D 12. Ovvero gli invii adiacenti degli operatori possono essere eseguiti in parallelo sulla GPU, a meno che non esista una barriera UAV intermedia tra di essi. Un modello di apprendimento automatico tipico contiene le dipendenze dei dati tra gli operatori; ad esempio, l'output di un operatore si inserisce nell'input di un altro. È quindi importante usare le barriere UAV per sincronizzare correttamente le invii.

DirectML garantisce che sia sempre in grado di leggere (e mai scrivere) i tensori di input. Garantisce inoltre che non produrrà mai Scritture in un tensore di output al di fuori dell'intervallo del membro [**DML_BUFFER_TENSOR_DESC:: TotalTensorSizeInBytes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) del tensore. Ciò significa che le dipendenze dei dati tra gli operatori in DirectML possono essere ragionate cercando solo le associazioni di input e di output di un operatore.

Queste garanzie consentono, ad esempio, di inviare due operatori che associano la stessa area di una risorsa come input, senza dover emettere una barriera UAV corrispondente. Questa operazione è sempre sicura perché DirectML non scrive mai nei tensori di input. Come altro esempio, è sempre possibile associare i tempi di output di due invii simultanei alla stessa risorsa Direct3D 12 (purché i loro tensori non si sovrappongano), perché DirectML non scrive mai all'esterno dei limiti di un tensore (come definito dall'DML_BUFFER_TENSOR_DESC di tensore **:: TotalTensorSizeInBytes**).

Poiché le barriere UAV sono una forma di sincronizzazione, l'uso superfluo delle barriere UAV potrebbe influire negativamente sulle prestazioni. È quindi consigliabile usare il numero minimo di barriere UAV necessarie per sincronizzare correttamente gli invii in un elenco di comandi.

### <a name="example-1"></a>Esempio 1

Nell'esempio seguente, l'output di un operatore di convoluzione viene inserito in un'attivazione ReLU, seguito da una normalizzazione batch.

```console
    CONVOLUTION (conv1)
         |
  ACTIVATION_RELU (relu1)
         |
BATCH_NORMALIZATION (batch1)
```

Poiché esiste una dipendenza tra i tre operatori, sarà necessaria una barriera UAV tra ogni dispatch successivo (vedere [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)).

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
2. `d3d12CommandList->ResourceBarrier(`**Barriera UAV**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**relu1**`)`
4. `d3d12CommandList->ResourceBarrier(`**Barriera UAV**`)`
5. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**Batch1**`)`

### <a name="example-2"></a>Esempio 2

```console
     MAX_POOLING (pool1)
        /    \
CONVOLUTION  CONVOLUTION
  (conv1)      (conv2)
        \    /
         JOIN (join1)
```

Qui l'output del pool viene inserito in due convoluzione, i cui output vengono quindi concatenati tramite l'operatore JOIN. Esiste una dipendenza dei dati tra e e `pool1` `conv1` , nonché `conv2` tra `conv1` e `conv2` e `join1` . Ecco un modo valido per eseguire questo grafico.

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**pool1**`)`
2. `d3d12CommandList->ResourceBarrier(`**Barriera UAV**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
4. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv2**`)`
5. `d3d12CommandList->ResourceBarrier(`**Barriera UAV**`)`
6. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**Join1**`)`

In questo caso, `conv1` e `conv2` sono in grado di eseguire contemporaneamente sulla GPU, che può migliorare le prestazioni.

## <a name="resource-barrier-state-requirements"></a>Requisiti dello stato della barriera delle risorse

Il chiamante è responsabile di assicurarsi che tutte le risorse Direct3D 12 si trovino nello stato di barriera delle risorse corretto prima di eseguire l'invio DirectML sulla GPU. DirectML non esegue alcuna barriera di transizione per conto dell'utente.

Prima dell'esecuzione di [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) sulla GPU, è necessario eseguire la transizione di tutte le risorse limitate allo stato **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** o a uno stato promuovibile in modo implicito a **D3D12_RESOURCE_STATE_UNORDERED_ACCESS**, ad esempio **D3D12_RESOURCE_STATE_COMMON**. Al termine della chiamata, le risorse rimangono nello stato **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** . Per altri dettagli, vedere [Binding in DirectML](dml-binding.md).

## <a name="see-also"></a>Vedi anche

* [Uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
* [Binding in DirectML](dml-binding.md)
