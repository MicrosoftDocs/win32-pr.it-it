---
description: L'interfaccia ISampleGrabberCB fornisce metodi di callback per il metodo ISampleGrabber::SetCallback. Se l'applicazione chiama tale metodo, deve implementare questa interfaccia. Per altre informazioni, vedere ISampleGrabber.
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Interfaccia ISampleGrabberCB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 822eef97ebd2ff169631f0e4d83cdfe3417388389e112851f5e77dcd7216acfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817503"
---
# <a name="isamplegrabbercb-interface"></a>Interfaccia ISampleGrabberCB

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`ISampleGrabberCB`L'interfaccia fornisce metodi di callback per il metodo [**ISampleGrabber::SetCallback.**](isamplegrabber-setcallback.md) Se l'applicazione chiama tale metodo, deve implementare questa interfaccia. Per altre informazioni, vedere [**ISampleGrabber.**](isamplegrabber.md)

## <a name="members"></a>Membri

**L'interfaccia ISampleGrabberCB** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISampleGrabberCB** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ISampleGrabberCB** include questi metodi.



| Metodo                                        | Descrizione                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**BufferCB**](isamplegrabbercb-buffercb.md) | Metodo di callback che riceve un puntatore al buffer di esempio.<br/> |
| [**SampleCB**](isamplegrabbercb-samplecb.md) | Metodo di callback che riceve un puntatore all'esempio multimediale.<br/>  |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
