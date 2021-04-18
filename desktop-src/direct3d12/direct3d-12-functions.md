---
title: Funzioni di base (grafica Direct3D 12)
description: Le funzioni seguenti sono dichiarate in d3d12. h.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: 99ec8516634a0a59262df9862e03732c9d6d579a
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "106299281"
---
# <a name="core-functions"></a>Funzioni di base

Le funzioni seguenti sono dichiarate in d3d12. h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | Crea un dispositivo che rappresenta l'adattatore di visualizzazione. |
| [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | Deserializza una firma radice per poter determinare la definizione del layout ([**D3D12 \_ root \_ Signature \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)). |
| [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | Genera un'interfaccia che può restituire la struttura dei dati deserializzati tramite [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc). |
| [**D3D12EnableExperimentalFeatures**](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | Consente un elenco di funzionalità sperimentali. |
| [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | Ottiene un'interfaccia di debug. |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | Serializza una firma radice versione 1,0 che può essere passata a [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature). |
| [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | Serializza una firma radice di qualsiasi versione che può essere passata a [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature). |

## <a name="related-topics"></a>Argomenti correlati

* [Riferimento principale](direct3d-12-core-reference.md)
* [Guida di riferimento a Direct3D 12](direct3d-12-reference.md)






