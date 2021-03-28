---
title: Registri-hs_5_0
description: Uno scafo dello shader è costituito da tre fasi distinte per la fase di controllo, la fase della divisione e la fase di join. Ogni fase dispone di un proprio set di registri di input e di output.
ms.assetid: 82F689EF-D3F4-40B5-9A2C-1F97F4CE6501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aca1377c7ca6b56434c361ba06b01cf659319f6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351896"
---
# <a name="registers---hs_5_0"></a>Registri-HS \_ 5 \_ 0

Un Hull shader è costituito da tre fasi distinte: fase del punto di controllo, fase della divisione e fase di join. Ogni fase dispone di un proprio set di registri di input e di output.

## <a name="control-point-phase"></a>Fase punto di controllo

\_ \_ \_ la fase del punto di controllo HS è un programma shader con il seguente modello di registro.

### <a name="input-registers"></a>Registri di input



| Tipo di registro                                     | Conteggio                 | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|---------------------------------------------------|-----------------------|-----|-----------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                 | 4096 (r \# + x \# \[ n \] )    | L/S | 4         | No               | nessuno     | Sì          |
| Matrice Temp indicizzabile a 32 bit (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] )    | L/S | 4         | Sì              | nessuno     | Sì          |
| Input a 32 bit ( \[ elemento vertice v \] \[ \] )             | 32 (elemento) \* 32 (Vert) | R   | 4         | Sì              | nessuno     | Sì          |
| vOutputControlPointID input UINT a 32 bit (23,7)     | 1                     | R   | 1         | No               | nessuno     | Sì          |
| PrimitiveID input UINT a 32 bit (vPrim)             | 1                     | R   | 1         | No               | N/D      | Sì          |
| Elemento in una risorsa di input (t \# )                | 128                   | R   | 128       | Sì              | nessuno     | Sì          |
| Campionatore/ \# i                                     | 16                    | R   | 1         | Sì              | nessuno     | Sì          |
| Guida di riferimento a ConstantBuffer ( \# \[ Indice CB \] )          | 15                    | R   | 4         | Sì              | nessuno     | Sì          |
| Riferimento ConstantBuffer immediato ( \[ Indice ICB \] ) | 1                     | R   | 4         | Sì (contenuto)   | nessuno     | Sì          |



 

### <a name="output-registers"></a>Registri di output



| Tipo di registro                           | Conteggio | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento dati vertex di output a 32 bit (o \# ) | 32    | W   | 4         | Sì              | nessuno     | Sì          |



 

Ogni registro di output della fase del punto di controllo di Hull shader è costituito da un vettore 4, di cui è possibile dichiarare fino a 32 registri. Sono stati dichiarati anche i punti di controllo dell'output da 1 a 32, con scalabilità della quantità di spazio di archiviazione necessaria. Viene ora fatto riferimento al numero massimo di scalabilità consentito di scalars in tutti gli output della fase del punto di controllo di Hull shader come \# \_ Max output CP \_ .

\#\_output CP \_ max = 3968 valori scalari.

Questo limite si basa su un punto di progettazione per un determinato hardware di 4096 di \* archiviazione a 32 bit. La quantità per l'output del punto di controllo è 3968 = 4096-128, ovvero 32 (punti di controllo) \* 4 (componenti) \* 32 (elementi)-4 (componenti) \* 32 (elementi). La sottrazione riserva 128 scalari (un punto di controllo) la quantità di spazio dedicato alla fase 2 e 3 di Hull shader. La scelta di riservare i valori scalari 128 per le costanti di patch, anziché consentire semplicemente a tutti i 4096 scalari di spazio di archiviazione, non è utilizzata dai punti di controllo di output: consente di gestire i limiti di un'altra progettazione hardware specifica. La fase del punto di controllo può dichiarare i punti di controllo dell'output di 32, ma non può essere completamente 32 elementi con 4 componenti ciascuno, perché lo spazio di archiviazione totale potrebbe essere troppo elevato.

## <a name="fork-phase"></a>Fase fork

I registri seguenti sono visibili nel modello di \_ fase della divisione HS \_ .

Le risorse di input (t \# ), i Samplers \# , i buffer costanti (CB \# ) e il buffer costante immediato (ICB) di seguito sono tutti stati condivisi con tutte le altre fasi di Hull shader. Ovvero dal punto di vista dell'API/DDI, lo scafo dello shader ha un singolo set di stato della risorsa di input per tutte le fasi. Questo è il fatto che dal punto di vista dell'API/DDI, lo scafo dello shader è un unico Atomic shader; le fasi al suo interno sono i dettagli di implementazione.

### <a name="input-registers"></a>Registri di input



| Tipo di registro                                                                         | Conteggio              | L/S | Dimension                           | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|---------------------------------------------------------------------------------------|--------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                                                     | 4096 (r \# + x \# \[ n \] ) | L/S | 4                                   | No               | nessuno     | Sì          |
| Matrice Temp indicizzabile a 32 bit (x \# \[ n \] )                                                | 4096 (r \# + x \# \[ n \] ) | L/S | 4                                   | Sì              | nessuno     | Sì          |
| Punti di controllo di input a 32 bit ( \[ elemento del vertice VICP \] \[ \] ) (fase del punto di pre-controllo)     | 32 vedere la nota di seguito  | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sì              | nessuno     | Sì          |
| Punti di controllo dell'output a 32 bit ( \[ elemento Vertex vocp \] \[ \] \] ) (fase del punto di post-controllo) | 32 vedere la nota di seguito  | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sì              | nessuno     | Sì          |
| PrimitiveID input UINT a 32 bit (vPrim)                                                 | 1                  | R   | 1                                   | No               | N/D      | Sì          |
| ForkInstanceID input UINT a 32 bit (23,8) (vForkInstanceID)                              | 1                  | R   | 1                                   | No               | N/D      | Sì          |
| Elemento in una risorsa di input (t \# )                                                    | 128                | R   | 128                                 | Sì              | nessuno     | Sì          |
| Campionatore/ \# i                                                                         | 16                 | R   | 1                                   | Sì              | nessuno     | Sì          |
| Guida di riferimento a ConstantBuffer ( \# \[ Indice CB \] )                                              | 15                 | R   | 4                                   | Sì              | nessuno     | Sì          |
| Riferimento ConstantBuffer immediato ( \[ Indice ICB \] )                                     | 1                  | R   | 4                                   | Sì (contenuto)   | nessuno     | Sì          |



 

> [!Note]
> Le dichiarazioni di registro del punto di controllo (VICP) della fase fork dello scafo shader devono essere qualsiasi subset, lungo \[ l' \] asse degli elementi, della fase di input del punto di controllo di Hull shader (fase del punto di controllo preliminare). Analogamente, le dichiarazioni per inserire i punti di controllo dell'output (vocp) devono essere qualsiasi subset, lungo l' \[ asse degli elementi \] , dei punti di controllo dell'output di Hull shader (fase di post-controllo).
> 
> Lungo l' \[ asse dei vertici \] , il numero di punti di controllo da leggere per ogni VICP e vocp deve essere simile a un subset del conteggio dei punti di controllo dell'input di Hull shader e del conteggio dei punti di controllo dell'output dello scafo shader, rispettivamente. Se, ad esempio, l'asse dei vertici dei registri vocp sono dichiarati con n vertici, che rende i punti di controllo di output della fase del punto di controllo \[ 0.. n-1 \] disponibile come input di sola lettura per la fase di fork.

### <a name="output-registers"></a>Registri di output



| Registrazione                                        | Conteggio               | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|-------------------------------------------------|---------------------|-----|-----------|------------------|----------|--------------|
| Elemento dati costante patch di output a 32 bit (o \# ) | 32 vedere la nota 1 di seguito | W   | 4         | Sì              | nessuno     | Sì          |



 

> [!Note]  
> Gli output delle fasi fork e join di Hull shader sono un set condiviso di registri vettoriali 4 4. Gli output di ogni programma fork o fase di join non possono sovrapporsi tra loro. I valori interpretati dal sistema, ad esempio TessFactors, provengono da questo spazio.

## <a name="join-phase"></a>Fase di join

I registri seguenti sono visibili nel modello di \_ fase join HS \_ . Sono disponibili tre set di registri di input: punti di controllo di input della fase di controllo (VICP), punti di controllo dell'output della fase del punto di controllo vocp (vocp) e costanti di patch (VCP). VPC è l'output aggregato di tutti i programmi della fase fork di Hull shader. I registri di output della fase di join \# di Hull shader si trovano nello stesso spazio del registro degli output della fase fork dello shader.

Le risorse di input (t \# ), i Samplers \# , i buffer costanti (CB \# ) e il buffer costante immediato (ICB) di seguito sono tutti stati condivisi con tutte le altre fasi di Hull shader. Ovvero dal punto di vista dell'API/DDI, lo scafo dello shader ha un singolo set di stato della risorsa di input per tutte le fasi. Questo è il fatto che dal punto di vista dell'API/DDI, lo scafo dello shader è un unico Atomic shader; le fasi al suo interno sono i dettagli di implementazione.

### <a name="input-registers"></a>Registri di input



| Tipo di registro                                                                       | Conteggio               | L/S | Dimension                           | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|-------------------------------------------------------------------------------------|---------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                                                   | 4096 (r \# + x \# \[ n \] )  | L/S | 4                                   | No               | nessuno     | Sì          |
| Matrice Temp indicizzabile a 32 bit (x \# \[ n \] )                                              | 4096 (r \# + x \# \[ n \] )  | L/S | 4                                   | Sì              | nessuno     | Sì          |
| Punti di controllo di input a 32 bit ( \[ elemento del vertice VICP \] \[ \] ) (fase del punto di pre-controllo)   | 32 vedere la nota 1 di seguito | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sì              | nessuno     | Sì          |
| Punti di controllo dell'output a 32 bit ( \[ elemento Vertex vocp \] \[ \] ) (fase del punto di post-controllo) | 32 vedere la nota 1 di seguito | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sì              | nessuno     | Sì          |
| Input a 32 bit ( \[ elemento VPC \] ) (dati costanti della patch)                                 | 32 vedere la nota 2 di seguito | R   | 4                                   | Sì              | nessuno     | Sì          |
| PrimitiveID input UINT a 32 bit (vPrim)                                               | 1                   | R   | 1                                   | No               | N/D      | Sì          |
| JoinInstanceID input UINT a 32 bit (vJoinInstanceID)                                  | 1                   | R   | 1                                   | No               | N/D      | Sì          |
| Elemento in una risorsa di input (t \# )                                                  | 128                 | R   | 128                                 | Sì              | nessuno     | Sì          |
| Campionatore/ \# i                                                                       | 16                  | R   | 1                                   | Sì              | nessuno     | Sì          |
| Guida di riferimento a ConstantBuffer ( \# \[ Indice CB \] )                                            | 15                  | R   | 4                                   | Sì              | nessuno     | Sì          |
| Riferimento ConstantBuffer immediato ( \[ Indice ICB \] )                                   | 1                   | R   | 4                                   | Sì (contenuto)   | nessuno     | Sì          |



 

**Nota 1:** Le dichiarazioni di registro del punto di controllo (VICP) della fase di join di Hull shader devono essere qualsiasi subset, lungo l' \[ asse degli elementi \] , della fase di input del punto di controllo di Hull shader (fase del punto di controllo preliminare). Analogamente, le dichiarazioni per inserire i punti di controllo dell'output (vocp) devono essere qualsiasi subset, lungo l' \[ asse degli elementi \] , dei punti di controllo dell'output di Hull shader (fase di post-controllo).

Lungo l' \[ asse dei vertici \] , il numero di punti di controllo da leggere per ogni VICP e vocp deve essere simile a un subset del conteggio dei punti di controllo dell'input di Hull shader e del conteggio dei punti di controllo dell'output dello scafo shader, rispettivamente. Se, ad esempio, l'asse dei vertici dei registri vocp sono dichiarati con n vertici, che rende i punti di controllo di output della fase del punto di controllo \[ 0.. n-1 \] disponibile come input di sola lettura per la fase di join.

**Nota 2:** Oltre all'input del punto di controllo, la fase di join Hull shader Considera anche come input i dati costanti della patch calcolati dal programma/i della fase di fork dello shader Hull. Questa operazione viene visualizzata in corrispondenza della fase fork dello scafo dello shader quando il VPC viene \# registrato. I registri VPC di input della fase di join di Hull shader \# condividono lo stesso spazio di registro dell'output o della fase di fork dello scafo dello shader \# . Le dichiarazioni dei \# registri o non devono sovrapporsi a una dichiarazione di output del programma o della fase fork dello scafo dello shader \# ; la fase di join Hull shader viene aggiunta all'output dei dati costanti della patch di aggregazione per Hull shader.

### <a name="output-registers"></a>Registri di output



| Tipo di registro                                   | Conteggio             | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|-------------------------------------------------|-------------------|-----|-----------|------------------|----------|--------------|
| Elemento dati costante patch di output a 32 bit (o \# ) | 32 vedere la nota di seguito | W   | 4         | Sì              | nessuno     | Sì          |



 

> [!Note]  
> Gli output delle fasi fork e join di Hull shader sono un set condiviso di registri vettoriali 4 4. Gli output di ogni programma fork o fase di join non possono sovrapporsi tra loro. I valori interpretati dal sistema, ad esempio TessFactors, provengono da questo spazio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




