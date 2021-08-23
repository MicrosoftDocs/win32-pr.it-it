---
description: Questi flag forniscono informazioni aggiuntive sui parametri dell'effetto.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 5314ae0a13f6b9f4e246cc61c33ce626f217a4d654de2f582d18027c952bd2a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607811"
---
# <a name="d3dx_parameter"></a>PARAMETRO \_ D3DX

Questi flag forniscono informazioni aggiuntive sui parametri dell'effetto.

Le costanti dei parametri effect vengono usate [**da D3DXPARAMETER \_ DESC.**](d3dxparameter-desc.md)



| Costante                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**ANNOTAZIONE DEI PARAMETRI D3DX \_ \_**</dt> </dl> | Questo parametro è contrassegnato come annotazione. Vedere [Aggiungere informazioni ai parametri degli effetti con annotazioni.](using-an-effect.md)<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**VALORE LETTERALE DEL PARAMETRO \_ \_ D3DX**</dt> </dl>          | Questo parametro è contrassegnato come valore letterale. I parametri letterali non possono cambiare dopo la compilazione, consentendo al compilatore di ottimizzarne l'utilizzo. I parametri condivisi non possono essere contrassegnati come valori letterali. Vedere [Utilizzi e valori letterali (Direct3D 9).](usages-and-literals.md) <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**PARAMETRO D3DX \_ \_ CONDIVISO**</dt> </dl>             | Il valore di un parametro verrà condiviso da tutti gli effetti nello stesso spazio dei nomi. La modifica del valore in un effetto lo modificherà in tutti gli effetti condivisi. Vedere [Condivisione di parametri.](cloning-and-sharing.md) **D3DX \_ PARAMETER \_ SHARED non** può essere combinato con **D3DX PARAMETER \_ \_ LITERAL** o **D3DX \_ PARAMETER \_ ANNOTATION**.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'effetto](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




