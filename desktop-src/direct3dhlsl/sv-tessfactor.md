---
title: SV_TessFactor
description: Definisce l'importo a mosaico per ogni bordo di una patch.
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
ms.openlocfilehash: 8fa49b19109985b590747098826199b33a32dd2d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976215"
---
# <a name="sv_tessfactor"></a>\_TESSFACTOR SV

Definisce l'importo a mosaico per ogni bordo di una patch.

## <a name="type"></a>Tipo



|            |                |
|------------|----------------|
| Tipo       | Topologia di input |
| float \[ 4\] | patch quad     |
| float \[ 3\] | patch Tri      |
| float \[ 2\] | isolinea        |



 

I fattori a mosaico devono essere dichiarati come matrice; non possono essere compressi in un singolo vettore.

## <a name="remarks"></a>Commenti

Il valore per il fattore a mosaico deve essere definito durante la funzione costante patch dello scafo shader.

Valore di output necessario per Hull shader se si usano patch quad o tri. Questo valore è anche un valore di input obbligatorio per lo shader del dominio in modo che corrisponda alle firme dei dati della patch-Constant tra le fasi a mosaico.

Per un elemento, il primo valore in SV \_ TessFactor è il fattore a mosaico a densità di riga, il secondo valore è il fattore a mosaico a dettaglio di riga.

### <a name="tri-patch-tessellation-factors"></a>Fattori a mosaico della patch Tri

Il primo componente fornisce il fattore geometrica per il bordo u = = 0 della patch. Il secondo componente fornisce il fattore geometrica per il bordo v = = 0 della patch. Il terzo componente fornisce il fattore geometrica per il bordo w = = 0 della patch.

### <a name="quad-patch-tessellation-factors"></a>Fattori a mosaico patch quad

Il primo componente fornisce il fattore geometrica per il bordo u = = 0 della patch. Il secondo componente fornisce il fattore geometrica per il bordo v = = 0 della patch. Il terzo componente fornisce il fattore geometrica per il bordo u = = 1 della patch. Il quarto componente fornisce il fattore geometrica per il bordo v = = 1 della patch. L'ordinamento dei bordi è in senso orario, a partire dal bordo u = = 0, che è il lato sinistro della patch, e dal bordo v = = 0, che è la parte superiore della patch.

Questa funzione è supportata nei tipi di shader seguenti:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Semantica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




