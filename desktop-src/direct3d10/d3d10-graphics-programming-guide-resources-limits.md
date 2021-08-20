---
description: Questa tabella contiene un elenco delle risorse minime supportate da Direct3D 10.
ms.assetid: 79c13aed-87bd-4875-9810-c3e078f58753
title: Limiti delle risorse (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93617f77306a85290f4846e0b767e971db5c627659aa8b4bbf8249e3e7a88f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100963"
---
# <a name="resource-limits-direct3d-10"></a>Limiti delle risorse (Direct3D 10)

Questa tabella contiene un elenco delle risorse minime supportate da Direct3D 10.



| Risorsa                                                                                               | Limite                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Numero di elementi in un buffer costante                                                                | 4096                                                 |
| Numero di texel (indipendenti dalle dimensioni dello struct) in un buffer                                              | 227 texel                                           |
| Dimensione Texture1D U                                                                                  | 8192                                                 |
| Dimensione Texture1DArray                                                                               | 512 sezioni di matrice                                     |
| Dimensione texture2D U/V                                                                                | 8192                                                 |
| Dimensione Texture2DArray                                                                               | 512 sezioni di matrice                                     |
| Dimensione Texture3D U/V/W                                                                              | 2048                                                 |
| Dimensione TextureCube                                                                                  | 8192                                                 |
| Dimensioni risorsa (in MB)                                                                                  | 128 MB                                              |
| Filtro anisotropo maxanisotropy                                                                    | 16                                                   |
| Dimensione della risorsa indirizzabile filtrando l'hardware                                                   | 8192 per dimensione                                   |
| Dimensioni delle risorse (in MB) indirizzabili da IA (dati di input o vertici) o VS/GS/PS (campione di punti)              | 128 MB                                              |
| Numero totale di visualizzazioni di risorse per contesto (ogni matrice conta come 1) (tutti i tipi di vista hanno un limite condiviso) | 220                                                  |
| Dimensioni della struttura del buffer (più elementi)                                                                  | 2048 byte                                           |
| Dimensioni dell'output del flusso                                                                                     | Uguale al numero di texel in un buffer (vedere sopra) |
| Conteggio vertici draw o DrawInstanced (inclusa la istanze)                                              | 232                                                  |
| DrawIndexed \[ Instanced \] () numero di vertici (incl. instancing)                                             | 232                                                  |
| Dati di output delle chiamate GS (vertici \* dei componenti)                                                     | 1024                                                 |
| Numero totale di oggetti campionatore per contesto                                                            | 4096                                                 |
| Numero totale di oggetti viewport/scissor per pipeline                                                  | 16                                                   |
| Numero totale di distanze clip/cull per vertice                                                         | 8                                                    |
| Numero totale di oggetti blend per contesto                                                              | 4096                                                 |
| Numero totale di oggetti depth/stencil per contesto                                                      | 4096                                                 |
| Numero totale di oggetti di stato del rasterizzatore per contesto                                                   | 4096                                                 |
| Numero massimo di campioni per pixel durante il multicampionamento                                                    | 32                                                   |
| Numero di vertici-elementi della risorsa shader (quattro componenti a 32 bit)                                          | 16                                                   |
| Common-shader core (quattro componenti a 32 bit) numero di registri temporanei (r \# + indicizzabile x \# \[ n \] )             | 4096                                                 |
| Slot common-shader core constant-buffer                                                               | 14                                                   |
| Slot di input-risorsa core dello shader comune                                                                | 128                                                  |
| Slot common-shader core sampler                                                                       | 16                                                   |
| Limite di annidamento delle subroutine core dello shader comune                                                            | 32                                                   |
| Limite di annidamento del controllo di flusso core dello shader comune                                                          | 64                                                   |
| Conteggio dei registri di input di vertex shader (quattro componenti a 32 bit)                                            | 16                                                   |
| Conteggio dei registri di output del vertex shader (quattro componenti a 32 bit)                                           | 16                                                   |
| Conteggio dei registri di input dello shader geometry (quattro componenti a 32 bit)                                          | 16                                                   |
| Conteggio dei registri di output dello shader geometry (quattro componenti a 32 bit)                                         | 32                                                   |
| Numero di registri di input pixel shader (quattro componenti a 32 bit)                                             | 32                                                   |
| Numero di registri di output pixel shader (quattro componenti a 32 bit)                                            | 8                                                    |
| Numero di registri di profondità dell'output pixel shader \* (componente a 1 bit a 32 bit)                                          | 1                                                    |
| Slot di risorse di input dell'assembler di input                                                             | 1                                                    |
| Slot di risorse di input vertice assembler di input                                                            | 16                                                   |



 

¹Apps può creare risorse superiori alle dimensioni massime delle risorse in alcuni componenti hardware grafici. Tuttavia, è consigliabile che le app mantenino le risorse inferiori alle dimensioni massime delle risorse per ottenere la massima compatibilità tra i fornitori di grafica. Il runtime garantisce solo che le allocazioni all'interno delle dimensioni massime delle risorse siano supportate da tutto l'hardware Direct3D 10. Se un'app tenta di allocare memoria per una risorsa entro le dimensioni massime della risorsa, il runtime ha esito negativo solo se il sistema operativo esaurisce le risorse. Se un'app tenta di allocare memoria per una risorsa superiore alle dimensioni massime della risorsa, il runtime può non riuscire perché il sistema operativo è estenso o l'hardware non supporta allocazioni superiori alle dimensioni massime della risorsa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



