---
description: "L'interfaccia ISampleGrabberCB fornisce metodi di callback per il metodo ISampleGrabber:: secallback. Se l'applicazione chiama tale metodo, deve implementare questa interfaccia. Per ulteriori informazioni, vedere ISampleGrabber."
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Interfaccia ISampleGrabberCB (qedit. h)
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
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326272"
---
# <a name="isamplegrabbercb-interface"></a>Interfaccia ISampleGrabberCB

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `ISampleGrabberCB` interfaccia fornisce metodi di callback per il metodo [**ISampleGrabber:: secallback**](isamplegrabber-setcallback.md) . Se l'applicazione chiama tale metodo, deve implementare questa interfaccia. Per ulteriori informazioni, vedere [**ISampleGrabber**](isamplegrabber.md).

## <a name="members"></a>Membri

L'interfaccia **ISampleGrabberCB** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISampleGrabberCB** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISampleGrabberCB** dispone di questi metodi.



| Metodo                                        | Descrizione                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**BufferCB**](isamplegrabbercb-buffercb.md) | Metodo di callback che riceve un puntatore al buffer di esempio.<br/> |
| [**SampleCB**](isamplegrabbercb-samplecb.md) | Metodo di callback che riceve un puntatore all'esempio multimediale.<br/>  |



 

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



 

 
