---
title: Strutture e funzioni helper per Direct3D 12
description: Queste strutture helper e funzioni helper vengono dichiarate in `d3dx12.h` .
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Funzioni helper
- Strutture helper
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b42bc9ae73f3537cc786a465feba596b3392401
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812173"
---
# <a name="helper-structures-and-functions-for-direct3d-12"></a>Strutture e funzioni helper per Direct3D 12

Queste strutture helper e funzioni helper vengono dichiarate in `d3dx12.h` .

`d3dx12.h` è disponibile separatamente dalle intestazioni Direct3D 12. È possibile scaricare `d3dx12.h` dalla [libreria helper D3D12.](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h)

È possibile usare queste strutture helper per creare e inizializzare strutture Direct3D. Queste strutture helper si comportano come classi C++. Ogni struttura helper ha in genere un costruttore predefinito, un costruttore esplicito, un distruttore e un operatore cast per la struttura D3D12 associata. Ogni struttura helper ha un prefisso "C" ed è associata a una struttura D3D12 che non ha il prefisso "C". La maggior parte delle strutture helper contiene metodi membro di inizializzazione, alcune contengono funzioni di confronto.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Interfacce helper per D3D12](helper-interfaces-for-d3d12.md) | Queste interfacce helper consentono in particolare di gestire le sottorisorse e vengono dichiarate in `d3dx12.h` .  |
| [Strutture helper per D3D12](helper-structures-for-d3d12.md) | Queste strutture helper consentono di inizializzare molte delle strutture Direct3D 12 e vengono dichiarate in `d3dx12.h` . |
| [Funzioni helper per D3D12](helper-functions-for-d3d12.md) | Queste funzioni helper consentono in particolare di gestire le sottorisorse e vengono dichiarate in `d3dx12.h` .  |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
