---
description: I parametri sono variabili di effetto.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parametri (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125583"
---
# <a name="parameters-direct3d-9"></a>Parametri (Direct3D 9)

I parametri sono variabili di effetto.

## <a name="syntax"></a>Sintassi

*ID tipo di utilizzo* \[ : espressione di  \] \[ < *annotazione* semantica > \] \[ =   \] .

I parametri possono essere letti e scritti dall'applicazione con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).

È possibile fare riferimento ai parametri nelle funzioni e nelle tecniche, in particolare nel lato destro delle assegnazioni di stato.



| Elemento                                                                                 | Descrizione                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*utilizzo*<br/>                   | Ambito del parametro. Vedere [utilizzi e valori letterali (Direct3D 9)](usages-and-literals.md).<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*tipo*<br/>                      | Qualsiasi [riferimento valido per](../direct3dhlsl/dx-graphics-hlsl-reference.md) il tipo HLSL.<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*ID*<br/>                            | Un nome univoco.<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*semantica*<br/>          | Tag che segue le regole dell'identificatore che in genere indicano l'uso del parametro. Deve essere un tipo particolare.<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*annotazioni*<br/> | Zero o più elementi di informazioni specifiche dell'utente. Può essere qualsiasi tipo. Vedere [aggiungere informazioni ai parametri di effetto con le annotazioni](using-an-effect.md).<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*espressione*<br/>    | Inizializza il valore del parametro. Vedere [espressioni (Direct3D 9)](expressions.md).<br/>                                                                  |



 

I parametri possono essere inizializzati in qualsiasi [riferimento valido per](../direct3dhlsl/dx-graphics-hlsl-reference.md) l'espressione HLSL che si riduce a un valore letterale.

I valori dei parametri non vengono modificati dall'esecuzione dell'assegnazione di stato o delle chiamate di funzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
