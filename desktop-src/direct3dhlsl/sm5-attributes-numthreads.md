---
title: numThreads
description: Definisce il numero di thread da eseguire in un gruppo a thread singolo quando viene inviato un compute shader (vedere sul ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399661"
---
# <a name="numthreads"></a>numThreads

Definisce il numero di thread da eseguire in un gruppo a thread singolo quando viene inviato un compute shader (vedere [**sul ID3D11DeviceContext::D la patch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).


```
numthreads(X, Y, Z)    
```



I valori X, Y e Z indicano le dimensioni del gruppo di thread in una direzione specifica e il totale di X \* Y \* z indica il numero di thread nel gruppo. La possibilità di specificare le dimensioni del gruppo di thread in tre dimensioni consente di accedere ai singoli thread in modo che le strutture di dati 2D e 3D siano logicamente.

Se, ad esempio, un compute shader sta eseguendo l'aggiunta di matrici 4x4, numThreads potrebbe essere impostato su numThreads (4, 4, 1) e l'indicizzazione nei singoli thread corrisponderà automaticamente alle voci della matrice. Il compute shader può anche dichiarare un gruppo di thread con lo stesso numero di thread (16) utilizzando numThreads (16, 1,1), tuttavia sarà necessario calcolare la voce della matrice corrente in base al numero di thread corrente.

I valori dei parametri consentiti per **numThreads** dipendono dalla versione compute shader.



| Compute Shader | Massimo Z | Numero massimo di thread (X \* Y \* Z) |
|----------------|-----------|---------------------------|
| cs \_ 4 \_ x       | 1         | 768                       |
| cs \_ 5 \_ 0       | 64        | 1024                      |



 

Nella figura seguente viene illustrata la relazione tra i parametri passati a [**sul ID3D11DeviceContext::D di patch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo numThreads, numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati ai thread ([SV \_ groupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![illustrazione della relazione tra dispatch, i gruppi di thread e i thread](images/threadgroupids.png)

Questo attributo è supportato nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del modello di shader 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 