---
description: Questa tabella contiene un elenco delle risorse minime supportate da Direct3D 10.
ms.assetid: 79c13aed-87bd-4875-9810-c3e078f58753
title: Limiti delle risorse (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ea3e3a181605e548c4e9f0a8b69691564163799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049291"
---
# <a name="resource-limits-direct3d-10"></a>Limiti delle risorse (Direct3D 10)

Questa tabella contiene un elenco delle risorse minime supportate da Direct3D 10.



| Risorsa                                                                                               | Limite                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Numero di elementi in un buffer costante                                                                | 4096                                                 |
| Numero di Texel (indipendente dalle dimensioni dello struct) in un buffer                                              | 227 Texel                                           |
| Dimensione Texture1D U                                                                                  | 8192                                                 |
| Dimensione Texture1DArray                                                                               | 512 sezioni di matrici                                     |
| Texture2D dimensione U/V                                                                                | 8192                                                 |
| Dimensione Texture2DArray                                                                               | 512 sezioni di matrici                                     |
| Dimensione Texture3D U/V/W                                                                              | 2048                                                 |
| Dimensione TextureCube                                                                                  | 8192                                                 |
| Dimensioni delle risorse (in MB)                                                                                  | 128 MB ¹                                              |
| Filtro anisotropico MaxAnisotropy                                                                    | 16                                                   |
| Dimensione della risorsa indirizzabile filtrando l'hardware                                                   | 8192 per dimensione                                   |
| Dimensioni delle risorse (in MB) indirizzabili da IA (dati di input o di vertice) o VS/GS/PS (esempio di punto)              | 128 MB ¹                                              |
| Numero totale di visualizzazioni di risorse per contesto (ogni matrice viene conteggiata come 1) (tutti i tipi di visualizzazione hanno un limite condiviso) | 220                                                  |
| Dimensione della struttura del buffer (più elementi)                                                                  | 2048 byte                                           |
| Dimensioni output flusso                                                                                     | Uguale al numero di Texel in un buffer (vedere sopra) |
| Conteggio vertici DrawInstanced (incluse le istanze)                                              | 232                                                  |
| DrawIndexed \[ \] () numero vertici (incl. instancement)                                             | 232                                                  |
| Dati di output della chiamata GS ( \* vertici dei componenti)                                                     | 1024                                                 |
| Numero totale di oggetti Sampler per contesto                                                            | 4096                                                 |
| Numero totale di oggetti Viewport/Scissor per pipeline                                                  | 16                                                   |
| Numero totale di distanze di clip/abbattimento per vertice                                                         | 8                                                    |
| Numero totale di oggetti Blend per contesto                                                              | 4096                                                 |
| Numero totale di oggetti depth/stencil per contesto                                                      | 4096                                                 |
| Numero totale di oggetti stato di rasterizzazione per contesto                                                   | 4096                                                 |
| Numero massimo di campioni per pixel durante il campionamento multiplo                                                    | 32                                                   |
| Numero di elementi del vertice delle risorse dello shader (componenti a 4 32 bit)                                          | 16                                                   |
| Common-shader Core (componenti a 4 32 bit) numero di registri temporanea (r \# + indicizzable x \# \[ n \] )             | 4096                                                 |
| Common-shader Core-slot buffer                                                               | 14                                                   |
| Input-slot di risorse core comuni shader                                                                | 128                                                  |
| Slot del campionatore core comuni shader                                                                       | 16                                                   |
| Sottoroutine di base di shader comuni-limite di annidamento                                                            | 32                                                   |
| Limite di nidificazione del controllo del flusso di base Common-shader                                                          | 64                                                   |
| Input vertex shader-conteggio registri (componenti a 4 32 bit)                                            | 16                                                   |
| Output vertex shader-conteggio registri (componenti a 4 32 bit)                                           | 16                                                   |
| Input geometry shader-conteggio registri (componenti a 4 32 bit)                                          | 16                                                   |
| Output geometry shader-conteggio registri (componenti a 4 32 bit)                                         | 32                                                   |
| Input pixel shader-conteggio registri (componenti a 4 32 bit)                                             | 32                                                   |
| Output pixel shader-conteggio registri (componenti a 4 32 bit)                                            | 8                                                    |
| Conteggio registri profondità di output pixel shader (componente a 32 bit \* 1)                                          | 1                                                    |
| Slot di input dell'indice dell'assembler di input                                                             | 1                                                    |
| Slot di input del vertice dell'assembler di input                                                            | 16                                                   |



 

¹ le app possono creare risorse maggiori delle dimensioni massime delle risorse in alcuni componenti hardware grafici. Tuttavia, è consigliabile che le applicazioni mantengano le risorse inferiori alle dimensioni massime della risorsa per ottenere la massima compatibilità tra i fornitori di grafica. Il runtime garantisce solo che le allocazioni nelle dimensioni massime delle risorse siano supportate da tutti i componenti hardware di Direct3D 10. Se un'app tenta di allocare memoria per una risorsa entro la dimensione massima delle risorse, il runtime non riesce a eseguire il tentativo solo se le risorse del sistema operativo sono esaurite. Se un'app tenta di allocare memoria per una risorsa superiore alle dimensioni massime delle risorse, il runtime può non riuscire perché il sistema operativo è troppo esteso o l'hardware non supporta le allocazioni oltre le dimensioni massime delle risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



