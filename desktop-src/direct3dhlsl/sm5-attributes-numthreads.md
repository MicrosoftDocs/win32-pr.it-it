---
title: numthreads
description: Definisce il numero di thread da eseguire in un singolo gruppo di thread quando viene inviato un compute shader (vedere ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f790548fb8ab629b7f6e7af345fa535d28a0d2216f570d02e851ce18618bbae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510120"
---
# <a name="numthreads"></a>numthreads

Definisce il numero di thread da eseguire in un singolo gruppo di thread quando viene inviato un compute shader (vedere [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).


```
numthreads(X, Y, Z)    
```



I valori X, Y e Z indicano le dimensioni del gruppo di thread in una direzione specifica e il totale di X Y Z indica il numero \* \* di thread nel gruppo. La possibilità di specificare le dimensioni del gruppo di thread in tre dimensioni consente l'accesso ai singoli thread in modo che le strutture di dati 2D e 3D siano logicamente 2D e 3D.

Ad esempio, se un compute shader esegue un'aggiunta di matrice 4x4, numthreads potrebbe essere impostato su numthreads(4,4,1) e l'indicizzazione nei singoli thread corrisponderebbe automaticamente alle voci della matrice. Lo shader di calcolo può anche dichiarare un gruppo di thread con lo stesso numero di thread (16) usando numthreads(16,1,1), ma deve quindi calcolare la voce della matrice corrente in base al numero di thread corrente.

I valori dei parametri consentiti per **numthreads** dipendono dalla versione dello shader di calcolo.



| Shader di calcolo | Z massimo | Numero massimo di thread (X \* Y \* Z) |
|----------------|-----------|---------------------------|
| cs \_ 4 \_ x       | 1         | 768                       |
| cs \_ 5 \_ 0       | 64        | 1024                      |



 

La figura seguente illustra la relazione tra i parametri passati [**a ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), i valori specificati nell'attributo numthreads, numthreads(10,8,3) e i valori che verranno passati allo shader di calcolo per i valori di sistema correlati al thread ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![Illustrazione della relazione tra dispatch, gruppi di thread e thread](images/threadgroupids.png)

Questo attributo è supportato nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del modello shader 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 