---
title: SV_TessFactor
description: Definisce la quantità a tessellazione su ogni bordo di una patch.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 808365fbcba4a1180c1838b94a6c098aa4c6f9ac
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999058"
---
# <a name="sv_tessfactor"></a>SV \_ TessFactor

Definisce la quantità a tessellazione su ogni bordo di una patch.

## <a name="type"></a>Tipo



|            |                |
|------------|----------------|
| Tipo       | Topologia di input |
| float \[ 4\] | quad patch     |
| float \[ 3\] | tri patch      |
| float \[ 2\] | isoline        |



 

I fattori a tessellazione devono essere dichiarati come matrice. non possono essere suddivisi in un singolo vettore.

## <a name="remarks"></a>Commenti

Il valore per il fattore a tessellazione deve essere definito durante la funzione costante patch dello hull shader.

Valore di output obbligatorio per lo hull shader se si usano patch quad o tri. Questo valore è anche un valore di input obbligatorio per il domain shader in modo che corrisponda alle firme di dati costanti per le patch tra le fasi a fasi.

Per un'isolinea, il primo valore in SV TessFactor è il fattore a tessellazione della densità della linea, il secondo valore è il fattore a trama \_ riga-dettaglio.

### <a name="tri-patch-tessellation-factors"></a>Tri Patch Tessellation Factors

Il primo componente fornisce il fattore di tesselation per il bordo u==0 della patch. Il secondo componente fornisce il fattore di tesselation per il bordo v==0 della patch. Il terzo componente fornisce il fattore di suddivisione a tesselation per il bordo w==0 della patch.

### <a name="quad-patch-tessellation-factors"></a>Quad Patch Tessellation Factors

Il primo componente fornisce il fattore di tesselation per il bordo u==0 della patch. Il secondo componente fornisce il fattore di tesselation per il bordo v==0 della patch. Il terzo componente fornisce il fattore di tesselation per il bordo u==1 della patch. Il quarto componente fornisce il fattore di tesselation per il bordo v==1 della patch. L'ordinamento dei bordi è in senso orario, a partire dal bordo u==0, ovvero il lato sinistro della patch, e dal bordo v==0, ovvero la parte superiore della patch.

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Semantica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




