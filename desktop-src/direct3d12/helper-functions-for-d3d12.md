---
title: Funzioni helper per Direct3D 12
description: Queste funzioni helper consentono in particolare di gestire le sottorisorse e sono dichiarate in `d3dx12.h` .
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funzioni helper
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9434bf916d7cb92116cdf4f7f6d86363b2eb51
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813184"
---
# <a name="helper-functions-for-direct3d-12"></a>Funzioni helper per Direct3D 12

Queste funzioni helper consentono in particolare di gestire le sottorisorse e sono dichiarate in `d3dx12.h` .

`d3dx12.h` è disponibile separatamente dalle intestazioni Direct3D 12. È possibile scaricare `d3dx12.h` dalla [libreria helper D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**CommandListCast**](commandlistcast.md) | Questo modello di funzione esegue il cast di un puntatore costante a qualsiasi elenco di comandi in un puntatore const a id3D12CommandList. |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md) | Calcola un indice di sottorisorsa per una trama. |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md) | Restituisce la sezione mip, la sezione di matrice e la sezione del piano che corrispondono all'indice di sottorisorsa specificato. |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) | Ottiene il numero di piani per il formato DXGI specificato per la scheda virtuale specificata **(id3D12Device).** |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md) | Indica se il layout è opaco. |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md) | Restituisce il tipo di oggetto secondario che corrisponde alla classe di base del tipo di sottooggetto passato. |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md) | Analizza una descrizione del flusso dello stato della pipeline, chiamando un callback definito dall'utente per ogni istanza di sottooggetto analizzata. |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md) | Consente di abilitare le funzionalità della firma radice 1.1 quando sono disponibili e non richiede la gestione di due percorsi di codice per la compilazione delle firme radice. Questo metodo helper ricostruisce una firma radice della versione 1.0 quando la versione 1.1 non è supportata. |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md) | Restituisce le dimensioni necessarie di un buffer da utilizzare per il caricamento dei dati. |
| [**Memcpysubresource**](memcpysubresource.md) | Copia una sottorisorsa riga per riga. |
| [**Aggiornamentiubresources**](updatesubresources1.md) | Aggiorna le sottorisorse, tutte le matrici di sottorisorse devono essere popolate, in genere chiamando [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). |
| [**Updatesubresources (allocazione heap)**](updatesubresources2.md) | Aggiorna le sottorisorse con un'implementazione di allocazione heap. |
| [**Updatesubresources (allocazione dello stack)**](updatesubresources3.md) | Aggiorna le sottorisorse con un'implementazione di allocazione dello stack. |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
* [Strutture e funzioni helper per D3D12](helper-structures-and-functions-for-d3d12.md)
