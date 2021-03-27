---
title: bem-PS
description: Applicare una trasformazione della mappa dell'ambiente di Bump Fake.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398264"
---
# <a name="bem---ps"></a>bem-PS

Applicare una trasformazione della mappa dell'ambiente di Bump Fake.

## <a name="syntax"></a>Sintassi



| bem DST. RG, src0, src1 |
|------------------------|



 

dove

-   DST. RG DST è il registro di destinazione. È necessario utilizzare la maschera di scrittura del componente rosso e verde.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bem                   |      |      |      | x    |      |      |       |      |       |



 

Questa istruzione esegue il calcolo seguente.


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



Regole per l'uso di bem:

1.  il bem deve essere visualizzato nella prima fase di uno shader, ovvero prima di un marcatore di fase.
2.  bem usa due slot di istruzione aritmetici.
3.  È consentito un solo utilizzo di questa istruzione per shader.
4.  Il writemask di destinazione deve essere. RG/.XY.
5.  Questa istruzione non può essere rilasciata.
6.  A parte la restrizione, la maschera di scrittura della destinazione è. RG, i modificatori nei modificatori di origine src0, src1 e istruzioni non sono vincolati.

## <a name="instruction-information"></a>Informazioni istruzioni



|                          |            |
|--------------------------|------------|
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




