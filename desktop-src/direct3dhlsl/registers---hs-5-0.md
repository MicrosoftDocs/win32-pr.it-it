---
title: Registri - hs_5_0
description: Uno hull shader è costituito da tre fasi distinte della fase del punto di controllo, della fase di fork e della fase di join. Ogni fase ha i propri set di registri di input e output.
ms.assetid: 82F689EF-D3F4-40B5-9A2C-1F97F4CE6501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3891130b4a952cb991615dbcc386e245d5eb8abedc2d8cec0b441eb6b3c2fbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854031"
---
# <a name="registers---hs_5_0"></a>Registri - hs \_ 5 \_ 0

Uno hull shader è costituito da tre fasi distinte: fase del punto di controllo, fase di fork e fase di join. Ogni fase ha i propri set di registri di input e output.

## <a name="control-point-phase"></a>Fase del punto di controllo

La fase \_ del punto di controllo \_ \_ hs è un programma shader con il modello di registro seguente.

### <a name="input-registers"></a>Registri di input



| Tipo di registro                                     | Conteggio                 | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede la DCL |
|---------------------------------------------------|-----------------------|-----|-----------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                 | 4096(r \# +x \# \[ n \] )    | L/S | 4         | No               | nessuno     | Sì          |
| Matrice temporanea indicizzabile a 32 bit (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] )    | L/S | 4         | Sì              | Nessuno     | Sì          |
| Input a 32 bit (elemento \[ vertice \] \[ v \] )             | 32(element) \* 32(vert) | R   | 4         | Sì              | Nessuno     | Sì          |
| Input UINT a 32 bit vOutputControlPointID(23.7)     | 1                     | R   | 1         | No               | nessuno     | Sì          |
| PrimitiveID di input UINT a 32 bit (vPrim)             | 1                     | R   | 1         | No               | N/D      | Sì          |
| Elemento in una risorsa di input (t \# )                | 128                   | R   | 128       | Sì              | Nessuno     | Sì          |
| Campionatore (s \# )                                     | 16                    | R   | 1         | Sì              | Nessuno     | Sì          |
| Riferimento ConstantBuffer (indice cb \# \[ \] )          | 15                    | R   | 4         | Sì              | Nessuno     | Sì          |
| Riferimento ConstantBuffer immediato (indice icb \[ \] ) | 1                     | R   | 4         | Sì (contenuto)   | Nessuno     | Sì          |



 

### <a name="output-registers"></a>Registri di output



| Tipo di registro                           | Conteggio | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede la DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento dati vertice di output a 32 bit (o \# ) | 32    | W   | 4         | Sì              | Nessuno     | Sì          |



 

Ogni registro di output della fase del punto di controllo dello shader è fino a un vettore a 4, di cui è possibile dichiarare fino a 32 registri. Sono inoltre dichiarati da 1 a 32 punti di controllo di output, che ridimensionano la quantità di spazio di archiviazione necessario. È possibile fare riferimento al numero aggregato massimo consentito di scalari in tutti gli output della fase del punto di controllo dello shader come \# cp \_ output \_ max.

\#cp \_ output max = \_ 3968 scalari.

Questo limite si basa su un punto di progettazione per un determinato hardware di archiviazione a 32 bit a 4096. \* La quantità per l'output del punto di controllo è 3968=4096-128, ovvero 32(punti di \* controllo) 4(componenti) \* 32(elementi) - 4(componenti) \* 32 (elementi). La sottrazione riserva 128 scalari (un punto di controllo) di spazio dedicato alla fase 2 e 3 dello hull shader. La scelta di riservare 128 scalari per le costanti patch, anziché consentire che la quantità di spazio di archiviazione 4096 sia inutilizzata dai punti di controllo di output, consente di soddisfare i limiti di un'altra progettazione hardware specifica. La fase del punto di controllo può dichiarare 32 punti di controllo di output, ma non possono essere completamente 32 elementi con 4 componenti ciascuno, perché lo spazio di archiviazione totale sarebbe troppo elevato.

## <a name="fork-phase"></a>Fase di fork

I registri seguenti sono visibili nel modello della fase \_ di fork hs. \_

Le risorse di input (t ), i campionatori (s ), i buffer costanti (cb ) e il buffer costante immediato \# \# (icb) riportati di seguito sono tutti stati condivisi con tutte le altre fasi \# di hull shader. Dal punto di vista dell'API/DDI, lo hull shader ha un singolo set di stato delle risorse di input per tutte le fasi. Ciò è associato al fatto che dal punto di vista dell'API/DDI, lo hull shader è un singolo shader atomico. Le fasi al suo interno sono i dettagli di implementazione.

### <a name="input-registers"></a>Registri di input



| Tipo di registro                                                                         | Conteggio              | L/S | Dimensione                           | Indicizzabile in base a r\# | Valori predefiniti | Richiede la DCL |
|---------------------------------------------------------------------------------------|--------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                                                     | 4096(r \# +x \# \[ n \] ) | L/S | 4                                   | No               | nessuno     | Sì          |
| Matrice temporanea indicizzabile a 32 bit (x \# \[ n \] )                                                | 4096(r \# +x \# \[ n \] ) | L/S | 4                                   | Sì              | Nessuno     | Sì          |
| Punti di controllo di input a 32 bit (elemento vertice vicp \[ \] \[ \] ) (fase del punto di pre-controllo)     | 32 Vedere la nota seguente  | R   | 4(componente) \* 32(elemento) \* 32(vert) | Sì              | Nessuno     | Sì          |
| Punti di controllo di output a 32 bit (elemento vertice vocp \[ \] \[ \] \] ) (fase del punto di post-controllo) | 32 Vedere la nota seguente  | R   | 4(componente) \* 32(elemento) \* 32(vert) | Sì              | Nessuno     | Sì          |
| PrimitiveID di input UINT a 32 bit (vPrim)                                                 | 1                  | R   | 1                                   | No               | N/D      | Sì          |
| UINT Input ForkInstanceID(23.8) (vForkInstanceID) a 32 bit                              | 1                  | R   | 1                                   | No               | N/D      | Sì          |
| Elemento in una risorsa di input (t \# )                                                    | 128                | R   | 128                                 | Sì              | Nessuno     | Sì          |
| Campionatore (s \# )                                                                         | 16                 | R   | 1                                   | Sì              | Nessuno     | Sì          |
| Riferimento ConstantBuffer (indice cb \# \[ \] )                                              | 15                 | R   | 4                                   | Sì              | Nessuno     | Sì          |
| Riferimento ConstantBuffer immediato (indice icb \[ \] )                                     | 1                  | R   | 4                                   | Sì (contenuto)   | Nessuno     | Sì          |



 

> [!Note]
> Le dichiarazioni del registro del punto di controllo di input (vicp) della fase di fork di hull shader devono essere qualsiasi subset, lungo l'asse degli elementi, dell'input del punto di controllo (fase del punto di \[ \] pre-controllo) dello shader. Analogamente, le dichiarazioni per l'input dei punti di controllo di output (vocp) devono essere qualsiasi subset, lungo l'asse degli elementi, dei punti di controllo di output dello shader (fase del punto di \[ \] post-controllo).
> 
> Lungo l'asse dei vertici, il numero di punti di controllo da leggere per ogni vicp e vocp deve essere analogamente un subset rispettivamente del conteggio dei punti di controllo di input e del conteggio dei punti di controllo dell'output di \[ \] hull shader. Ad esempio, se l'asse dei vertici dei registri vocp viene dichiarato con n vertici, i punti di controllo di output della fase di controllo 0..n-1 saranno disponibili come input di sola lettura per la fase \[ \] di fork.

### <a name="output-registers"></a>Registri di output



| Registrazione                                        | Conteggio               | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede la DCL |
|-------------------------------------------------|---------------------|-----|-----------|------------------|----------|--------------|
| Elemento dati costante patch di output a 32 bit (o \# ) | 32 Vedere la nota 1 di seguito | W   | 4         | Sì              | Nessuno     | Sì          |



 

> [!Note]  
> Gli output della fase di fork e join dello hull shader sono un set condiviso di 4 registri a 4 vettori. Gli output di ogni programma di fase di fork o join non possono sovrapporsi tra loro. I valori interpretati dal sistema, ad esempio TessFactors, escno da questo spazio.

## <a name="join-phase"></a>Fase di join

I registri seguenti sono visibili nel modello della fase \_ di join \_ hs. Esistono tre set di registri di input: punti di controllo di input della fase di controllo (vicp), punti di controllo di output della fase del punto di controllo vocp (vocp) e costanti di patch (vcp). vpc è l'output aggregato di tutti i programmi della fase di fork dello hull shader. I registri o dell'output della fase di join dello hull shader sono nello stesso spazio di registrazione degli output della fase \# di fork dello hulll shader.

Le risorse di input (t ), i campionatori (s), i buffer costanti (cb ) e il buffer costante immediato \# \# (icb) seguenti sono tutti stati condivisi con tutte le altre fasi \# dello hull shader. Dal punto di vista api/DDI, lo hull shader ha un singolo set di stato della risorsa di input per tutte le fasi. Questo vale per il fatto che dal punto di vista api/DDI, lo hull shader è un singolo shader atomico; le fasi al suo interno sono i dettagli di implementazione.

### <a name="input-registers"></a>Registri di input



| Tipo di registrazione                                                                       | Conteggio               | L/S | Dimensione                           | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|-------------------------------------------------------------------------------------|---------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                                                   | 4096(r \# +x \# \[ n \] )  | L/S | 4                                   | No               | nessuno     | Sì          |
| Matrice temporanea indicizzabile a 32 bit (x \# \[ n \] )                                              | 4096(r \# +x \# \[ n \] )  | L/S | 4                                   | Sì              | Nessuno     | Sì          |
| Punti di controllo di input a 32 bit (elemento vertice vicp \[ \] \[ \] ) (fase del punto di controllo preliminare)   | 32 Vedere la nota 1 riportata di seguito | R   | 4(componente) \* 32(elemento) \* 32(vert) | Sì              | Nessuno     | Sì          |
| Punti di controllo di output a 32 bit (elemento vertice vocp \[ \] \[ \] ) (fase post-punto di controllo) | 32 Vedere la nota 1 riportata di seguito | R   | 4(componente) \* 32(elemento) \* 32(vert) | Sì              | Nessuno     | Sì          |
| Input a 32 bit (elemento vpc \[ \] ) (Patch Constant Data)                                 | 32 Vedere la nota 2 riportata di seguito | R   | 4                                   | Sì              | Nessuno     | Sì          |
| PrimitiveID di input UINT a 32 bit (vPrim)                                               | 1                   | R   | 1                                   | No               | N/D      | Sì          |
| UINT Input JoinInstanceID a 32 bit (vJoinInstanceID)                                  | 1                   | R   | 1                                   | No               | N/D      | Sì          |
| Elemento in una risorsa di input (t \# )                                                  | 128                 | R   | 128                                 | Sì              | Nessuno     | Sì          |
| Campionatore \# (s)                                                                       | 16                  | R   | 1                                   | Sì              | Nessuno     | Sì          |
| Informazioni di riferimento su ConstantBuffer (indice cb \# \[ \] )                                            | 15                  | R   | 4                                   | Sì              | Nessuno     | Sì          |
| Riferimento immediato a ConstantBuffer (indice icb \[ \] )                                   | 1                   | R   | 4                                   | Sì (contenuto)   | Nessuno     | Sì          |



 

**Nota 1:** Le dichiarazioni vicp (Input Control Point Register) della fase di join dello hull shader devono essere qualsiasi subset, lungo l'asse degli elementi, dell'input del punto di controllo \[ \] hull shader (fase del punto di pre-controllo). Analogamente, le dichiarazioni per l'input dei punti di controllo di output (vocp) devono essere qualsiasi subset, lungo l'asse degli elementi, dei punti di controllo di output dello hull shader (fase del punto \[ \] di post-controllo).

Lungo l'asse dei vertici, il numero di punti di controllo da leggere per ogni vicp e vocp deve essere analogamente un subset del conteggio dei punti di controllo di input dello hull shader e del conteggio dei punti di controllo di output dello \[ \] hull shader, rispettivamente. Ad esempio, se l'asse dei vertici dei registri vocp viene dichiarato con n vertici, i punti di controllo di output della fase di controllo \[ 0..n-1 saranno disponibili come input di sola lettura per la fase \] di join.

**Nota 2:** Oltre all'input del punto di controllo, la fase di join dello hull shader vede anche come input i dati costanti della patch calcolati dai programmi della fase di fork dello hull shader. Questo viene visualizzato nella fase di fork dello hull shader durante la registrazione \# del vpc. I registri vpc di input della fase di join dello hull shader condividono lo stesso spazio di registrazione dei registri o dell'output della fase \# di fork dello hull \# shader. Le dichiarazioni dei registri o non devono sovrapporsi ad alcuna dichiarazione di output o programma della fase di fork dello hull shader. La fase di join dello hull shader viene aggiunta all'output dei dati delle costanti della patch aggregata per lo \# \# shader hull.

### <a name="output-registers"></a>Registri di output



| Tipo di registrazione                                   | Conteggio             | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|-------------------------------------------------|-------------------|-----|-----------|------------------|----------|--------------|
| Elemento dati costanti patch di output a 32 bit (o \# ) | 32 Vedere la nota seguente | W   | 4         | Sì              | Nessuno     | Sì          |



 

> [!Note]  
> Gli output della fase di fork e join dello hull shader sono un set condiviso di 4 registri a 4 vettori. Gli output di ogni programma di fase di fork o join non possono sovrapporsi tra loro. I valori interpretati dal sistema, ad esempio TessFactors, escno da questo spazio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




