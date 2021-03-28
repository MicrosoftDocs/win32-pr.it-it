---
title: Registro delle coordinate di trama (riferimenti per HLSL PS)
description: Registro di input del pixel shader contenente coordinate di trama.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104976511"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a>Registro delle coordinate di trama (riferimenti per HLSL PS)

Registro di input del pixel shader contenente coordinate di trama.



| Versioni pixel shader       | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro coordinate trama |      |      |      |      | x    | x     | x    | x    | x     |



 

Un registro delle coordinate di trama contiene dati delle coordinate di trama. Prima di utilizzare un registro delle coordinate di trama, è necessario dichiararlo tramite una dichiarazione pixel shader. Per informazioni dettagliate su come dichiarare un registro di trama, vedere [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).

Inoltre, di seguito sono riportate alcune altre proprietà dei registri delle coordinate di trama.

-   Sono presenti otto registri delle coordinate di trama di pixel shader, da T0 a T7.
-   Si tratta di registri di sola lettura.
-   Contengono valori RGBA a quattro componenti iterati dai vertici di input.
-   Contengono valori di dati ad alta precisione e di intervallo dinamico elevati interpolati dai dati dei vertici. I valori vengono generati con l'interpolazione corretta della prospettiva. I dati sono di precisione a virgola mobile e sono firmati.
-   È presente un massimo di uno in un'unica istruzione.
-   Più letture di un registro delle coordinate di trama in uno shader devono usare una [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)identica.
-   Il modificatore di precisione parziale facoltativo \[ \_ PP \] si applica alle letture dipendenti. Questo perché la precisione parziale influiscono sulle operazioni aritmetiche che coinvolgono il registro delle coordinate di trama. Non influirà sulla precisione delle istruzioni per gli indirizzi di trama perché non influisce sugli iteratori delle coordinate di trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




