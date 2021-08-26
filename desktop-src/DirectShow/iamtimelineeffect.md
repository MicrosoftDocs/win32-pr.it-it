---
description: L'interfaccia IAMTimelineEffect fornisce metodi per modificare gli effetti audio e video in DirectShow Editing Services (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interfaccia IAMTimelineEffect (Qedit.h)
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
ms.openlocfilehash: f710693c967e1f0ac73c69534e8ac90a65d6603e749cd2aeae6a355ed8517415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052761"
---
# <a name="iamtimelineeffect-interface"></a>Interfaccia IAMTimelineEffect

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

L'interfaccia fornisce metodi per modificare gli effetti audio e `IAMTimelineEffect` video in DirectShow Editing [Services](directshow-editing-services.md) (DES). È possibile aggiungere un effetto a qualsiasi oggetto sequenza temporale che espone [**l'interfaccia IAMTimelineEffectable.**](iamtimelineeffectable.md) Per impostare le proprietà di un effetto, usare [**l'interfaccia IPropertySetter.**](ipropertysetter.md)

L'oggetto effetto DES è in realtà un wrapper per uno degli altri due oggetti:

-   Per gli effetti audio, qualsiasi filtro DirectShow effetto audio.
-   Per gli effetti video e l'oggetto DirectX Transform a 1 input.

Microsoft non supporta più lo sviluppo di oggetti DirectX Transform di terze parti.

Per specificare il filtro o l'oggetto DirectX Transform per un effetto, chiamare il metodo [**IAMTimelineObj::SetSubObjectGUID.**](iamtimelineobj-setsubobjectguid.md)

Per creare un oggetto effetto, chiamare [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con il valore TIMELINE \_ MAJOR TYPE \_ \_ EFFECT. È possibile eseguire una query sul puntatore [**IAMTimelineObj restituito**](iamtimelineobj.md) per `IAMTimelineEffect` l'interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IAMTimelineEffect** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineEffect** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IAMTimelineEffect.**



| Metodo                                                           | Descrizione                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**EffectGetPriority**](iamtimelineeffect-effectgetpriority.md) | Recupera il livello di priorità dell'effetto.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di effetti e transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
