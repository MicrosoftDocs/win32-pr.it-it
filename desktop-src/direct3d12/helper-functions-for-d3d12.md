---
title: Funzioni helper per D3D12
description: Queste funzioni helper consentono in particolare di gestire le sottorisorse e vengono dichiarate in d3dx12.h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funzioni helper
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10736d91da0e2c4efa2a3c981ab5c4f64e2af86d
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102136"
---
# <a name="helper-functions-for-d3d12"></a>Funzioni helper per D3D12

Queste funzioni helper consentono in particolare di gestire le sottorisorse e vengono dichiarate in **d3dx12.h**.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommandListCast**](commandlistcast.md)<br/>                                     | Questo modello di funzione esegue il cast di un puntatore costante a qualsiasi elenco di comandi in un puntatore const a id3D12CommandList.<br/>                                                                                                                               |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md)<br/>                                   | Calcola un indice di sottorisorsa per una trama. <br/>                                                                                                                                                                                                  |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md)<br/>                         | Restituisce la sezione mip, la sezione di matrice e la sezione del piano che corrispondono all'indice di sottorisorsa specificato. <br/>                                                                                                                                        |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md)<br/>                           | Ottiene il numero di piani per il formato DXGI specificato per la scheda virtuale specificata **(ID3D12Device).** <br/>                                                                                                                               |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md)<br/>                                     | Indica se il layout è opaco.<br/>                                                                                                                                                                                                         |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md)<br/>                       | Restituisce il tipo di oggetto secondario che corrisponde alla classe di base del tipo di oggetto secondario passato.<br/>                                                                                                                                                  |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md)<br/>                    | Analizza una descrizione del flusso di stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di oggetto secondario analizzata.<br/>                                                                                                                                 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md)<br/> | Consente di abilitare le funzionalità della firma radice 1.1 quando sono disponibili e non richiede la gestione di due percorsi di codice per la compilazione delle firme radice. Questo metodo helper ricostruisce una firma radice della versione 1.0 quando la versione 1.1 non è supportata.<br/> |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md)<br/>                     | Restituisce le dimensioni richieste di un buffer da utilizzare per il caricamento dei dati. <br/>                                                                                                                                                                              |
| [**Memcpysubresource**](memcpysubresource.md)<br/>                                         | Copia una sottorisorsa riga per riga. <br/>                                                                                                                                                                                                               |
| [**Aggiornamentiubresources**](updatesubresources1.md)<br/>                                      | Aggiorna le sottorisorse. Tutte le matrici di sottorisorse devono essere popolate, in genere chiamando [**ID3D12Device::GetCopyablePrints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). <br/>                                                                  |
| [**Updatesubresources (allocazione heap)**](updatesubresources2.md)<br/>                    | Aggiorna le sottorisorse con un'implementazione di allocazione heap. <br/>                                                                                                                                                                                    |
| [**Updatesubresources (allocazione dello stack)**](updatesubresources3.md)<br/>                   | Aggiorna le sottorisorse con un'implementazione di allocazione dello stack. <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Strutture e funzioni helper per D3D12](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





