---
description: L'interfaccia IRenderEngine2 consente all'applicazione di sostituire il filtro di ridimensionamento video predefinito usato DirectShow Editing Services (DES). Il motore di rendering di base e il motore di rendering intelligente supportano entrambe questa interfaccia.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interfaccia IRenderEngine2 (Qedit.h)
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
ms.openlocfilehash: 39f1bc68fc6cd76e87d1998047cb211b3a8aa8e263c90e0494c7eaf15d52f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818509"
---
# <a name="irenderengine2-interface"></a>Interfaccia IRenderEngine2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

L'interfaccia consente all'applicazione di sostituire il filtro di ridimensionamento video predefinito usato `IRenderEngine2` DirectShow Editing Services (DES). Il [motore di rendering di base](basic-render-engine.md) e il motore di rendering [intelligente](smart-render-engine.md) supportano entrambe questa interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IRenderEngine2** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IRenderEngine2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IRenderEngine2** include questi metodi.



| Metodo                                                  | Descrizione                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**SetResizerGUID**](irenderengine2-setresizerguid.md) | Specifica il CLSID di un filtro di ridimensionamento personalizzato fornito dall'applicazione.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9.0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Fornire un ridimensionamento video personalizzato](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
