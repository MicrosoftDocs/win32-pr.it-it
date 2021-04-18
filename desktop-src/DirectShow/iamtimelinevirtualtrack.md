---
description: L'interfaccia IAMTimelineVirtualTrack fornisce metodi per l'uso di tracce virtuali in servizi di modifica DirectShow (DES). Le composizioni e le tracce supportano questa interfaccia.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Interfaccia IAMTimelineVirtualTrack (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327424"
---
# <a name="iamtimelinevirtualtrack-interface"></a>Interfaccia IAMTimelineVirtualTrack

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineVirtualTrack` interfaccia fornisce metodi per l'utilizzo di tracce virtuali in [servizi di modifica DirectShow](directshow-editing-services.md) (des). Le composizioni e le tracce supportano questa interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineVirtualTrack** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineVirtualTrack** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineVirtualTrack** dispone di questi metodi.



| Metodo                                                               | Descrizione                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [**SetTrackDirty**](iamtimelinevirtualtrack-settrackdirty.md)       | Non supportata.<br/>                         |
| [**TrackGetPriority**](iamtimelinevirtualtrack-trackgetpriority.md) | Recupera il livello di priorità dell'oggetto.<br/> |



 

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



 

 
