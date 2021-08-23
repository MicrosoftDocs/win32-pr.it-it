---
description: I parametri sono variabili di effetto.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parametri (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc28d1410180aac54daf306fe586694cfa1b7f4123403efc606a77385d088326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606681"
---
# <a name="parameters-direct3d-9"></a>Parametri (Direct3D 9)

I parametri sono variabili di effetto.

## <a name="syntax"></a>Sintassi

*ID tipo di utilizzo:* \[ *espressione* di \] \[ < *annotazione* > \] \[ =  *semantica;* \]

I parametri possono essere letti e scritti dall'applicazione con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).

È possibile fare riferimento ai parametri nelle funzioni e nelle tecniche (in particolare, sul lato destro delle assegnazioni di stato).



| Elemento                                                                                 | Descrizione                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*Utilizzo*<br/>                   | Ambito del parametro. Vedere [Utilizzi e valori letterali (Direct3D 9).](usages-and-literals.md)<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*digitare*<br/>                      | Qualsiasi riferimento [valido per il tipo HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*Id*<br/>                            | Un nome univoco.<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*Semantica*<br/>          | Tag che segue le regole dell'identificatore che in genere indica l'utilizzo del parametro . Deve essere un tipo specifico.<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotazioni*<br/> | Zero o più informazioni specifiche dell'utente. Può essere di qualsiasi tipo. Vedere [Aggiungere informazioni ai parametri degli effetti con annotazioni](using-an-effect.md).<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*Espressione*<br/>    | Inizializza il valore del parametro. Vedere [Espressioni (Direct3D 9).](expressions.md)<br/>                                                                  |



 

I parametri possono essere inizializzati in qualsiasi espressione [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) valida che riduce a un valore letterale.

I valori dei parametri non vengono modificati dall'esecuzione di chiamate di funzione o di assegnazione di stato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
