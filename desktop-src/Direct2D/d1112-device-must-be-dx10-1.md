---
title: Il dispositivo D1112 deve essere DX11
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: Il dispositivo associato alla superficie di DXGI deve essere un dispositivo D3D11.
keywords:
- Il dispositivo D1112 deve essere Direct2D DX11
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b4204e04332876db9145baba9888dbb2d339eff9
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104046454"
---
# <a name="d1112-device-must-be-dx11"></a>D1112: il dispositivo deve essere DX11

Il dispositivo associato alla superficie di DXGI deve essere un dispositivo D3D11.



|             |         |
|-------------|---------|
| Livello di errore | Avviso |



 

## <a name="possible-causes"></a>Possibili cause

Si è verificato un tentativo di usare [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) con una superficie DXGI creata da un dispositivo non Direct3D11.

 

 




