---
title: Il dispositivo D1112 deve essere DX11
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: Il dispositivo associato alla superficie DXGI deve essere un dispositivo D3D11.
keywords:
- Il dispositivo D1112 deve essere DX11 Direct2D
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 24c8bf123d9e00eff90f216676ec03f7d68cbe692511118c36c1433cbf0354d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758111"
---
# <a name="d1112-device-must-be-dx11"></a>D1112: Il dispositivo deve essere DX11

Il dispositivo associato alla superficie DXGI deve essere un dispositivo D3D11.



| &nbsp;      |  &nbsp; |
|-------------|---------|
| Livello di errore | Avviso |



 

## <a name="possible-causes"></a>Possibili cause

Si è tentato di usare [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) con una superficie DXGI creata da un dispositivo non Direct3D11.

 

 




