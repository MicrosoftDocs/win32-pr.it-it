---
description: Questi flag forniscono informazioni aggiuntive sui parametri di effetto.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
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
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322893"
---
# <a name="d3dx_parameter"></a>\_Parametro D3DX

Questi flag forniscono informazioni aggiuntive sui parametri di effetto.

Le costanti del parametro Effect vengono usate da [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).



| Costante                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**\_Annotazione del parametro D3DX \_**</dt> </dl> | Questo parametro è contrassegnato come annotazione. Vedere [aggiungere informazioni ai parametri di effetto con le annotazioni](using-an-effect.md).<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**\_ \_ Valore letterale parametro D3DX**</dt> </dl>          | Questo parametro è contrassegnato come valore letterale. I parametri letterali non possono essere modificati dopo la compilazione, consentendo al compilatore di ottimizzare l'utilizzo. I parametri condivisi non possono essere contrassegnati come valori letterali. Vedere [utilizzi e valori letterali (Direct3D 9)](usages-and-literals.md). <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**\_Parametro D3DX \_ condiviso**</dt> </dl>             | Il valore di un parametro verrà condiviso da tutti gli effetti nello stesso spazio dei nomi. Se si modifica il valore in un effetto, questo verrà modificato in tutti gli effetti condivisi. Vedere [condivisione di parametri](cloning-and-sharing.md). **D3DX \_ Impossibile combinare il parametro \_ Shared** con l' **\_ \_ annotazione** del parametro D3DX o D3DX. **\_ \_**<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti effetto](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




