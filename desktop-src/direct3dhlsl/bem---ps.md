---
title: bem - ps
description: Applicare una trasformazione mappa dell'ambiente di urto fittizia.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129930"
---
# <a name="bem---ps"></a>bem - ps

Applicare una trasformazione mappa dell'ambiente di urto fittizia.

## <a name="syntax"></a>Sintassi



| bem dst.rg, src0, src1 |
|------------------------|



 

dove

-   dst.rg dst è il registro di destinazione. È necessario usare la maschera di scrittura del componente rosso e verde.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Bem                   |      |      |      | x    |      |      |       |      |       |



 

Questa istruzione esegue il calcolo seguente.


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



Regole per l'uso di bem:

1.  bem deve essere visualizzato nella prima fase di uno shader, ovvero prima di un marcatore di fase.
2.  bem utilizza due slot di istruzioni aritmetiche.
3.  È consentito un solo uso di questa istruzione per shader.
4.  La maschera di scrittura di destinazione deve essere .rg /.xy.
5.  Questa istruzione non può essere co-rilasciata.
6.  A parte la restrizione che destination write mask è rg, i modificatori di origine src0, src1 e i modificatori di istruzione non sono vincolati.

## <a name="instruction-information"></a>Informazioni sulle istruzioni



| Requisito                         | Valore           |
|--------------------------|------------|
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




