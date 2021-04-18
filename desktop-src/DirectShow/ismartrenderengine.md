---
description: L'interfaccia ISmartRenderEngine fornisce metodi che supportano la ricompressione intelligente nei servizi di modifica DirectShow (DES). Il motore di rendering intelligente espone questa interfaccia.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Interfaccia ISmartRenderEngine (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327422"
---
# <a name="ismartrenderengine-interface"></a>Interfaccia ISmartRenderEngine

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `ISmartRenderEngine` interfaccia fornisce metodi che supportano la ricompressione intelligente in [DirectShow editing Services](directshow-editing-services.md) (des). Il motore di rendering intelligente espone questa interfaccia.

## <a name="members"></a>Membri

L'interfaccia **ISmartRenderEngine** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISmartRenderEngine** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISmartRenderEngine** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md)   | Recupera il filtro di compressione per il gruppo specificato.<br/>                 |
| [**SetFindCompressorCB**](ismartrenderengine-setfindcompressorcb.md) | Non implementato.<br/>                                                          |
| [**SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md)   | Specifica un filtro di compressione da usare quando si esegue il rendering del gruppo specificato.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Rendering di un progetto](rendering-a-project.md)
</dt> </dl>

 

 
