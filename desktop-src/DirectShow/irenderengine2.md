---
description: L'interfaccia IRenderEngine2 consente all'applicazione di sostituire il filtro di ridimensionamento video predefinito usato da DirectShow editing Services (DES). Il motore di rendering di base e il motore di rendering intelligente supportano entrambi questa interfaccia.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interfaccia IRenderEngine2 (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332572"
---
# <a name="irenderengine2-interface"></a>Interfaccia IRenderEngine2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IRenderEngine2` interfaccia consente all'applicazione di sostituire il filtro di ridimensionamento video predefinito usato da DirectShow editing Services (des). Il [motore di rendering di base](basic-render-engine.md) e il [motore di rendering intelligente](smart-render-engine.md) supportano entrambi questa interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IRenderEngine2** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IRenderEngine2** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**SetResizerGUID**](irenderengine2-setresizerguid.md) | Specifica il CLSID di un filtro di ridimensionamento personalizzato fornito dall'applicazione.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9,0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Creazione di una ridisposizione video personalizzata](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
