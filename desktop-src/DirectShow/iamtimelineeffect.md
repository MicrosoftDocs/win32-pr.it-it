---
description: L'interfaccia IAMTimelineEffect fornisce i metodi per modificare gli effetti audio e video in DirectShow editing Services (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interfaccia IAMTimelineEffect (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333700"
---
# <a name="iamtimelineeffect-interface"></a>Interfaccia IAMTimelineEffect

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineEffect` interfaccia fornisce i metodi per modificare gli effetti audio e video in [DirectShow editing Services](directshow-editing-services.md) (des). Un effetto può essere aggiunto a qualsiasi oggetto sequenza temporale che espone l'interfaccia [**IAMTimelineEffectable**](iamtimelineeffectable.md) . Per impostare le proprietà di un effetto, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .

L'oggetto effetto DES è effettivamente un wrapper per uno degli altri due oggetti:

-   Per gli effetti audio, qualsiasi filtro effetto audio DirectShow.
-   Per gli effetti video e l'oggetto trasformazione DirectX con 1 input.

Microsoft non supporta più lo sviluppo di oggetti di trasformazione DirectX di terze parti.

Per specificare l'oggetto filtro o trasformazione DirectX per un effetto, chiamare il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Per creare un oggetto Effect, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con l'effetto di tipo principale della sequenza temporale del valore \_ \_ \_ . È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l' `IAMTimelineEffect` interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineEffect** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineEffect** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineEffect** dispone di questi metodi.



| Metodo                                                           | Descrizione                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**EffectGetPriority**](iamtimelineeffect-effectgetpriority.md) | Recupera il livello di priorità dell'effetto.<br/> |



 

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

[Utilizzo degli effetti e delle transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
