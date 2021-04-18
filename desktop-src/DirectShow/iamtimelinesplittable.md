---
description: L'interfaccia IAMTimelineSplittable suddivide un oggetto Timeline in servizi di modifica DirectShow (DES). Le origini, gli effetti, le transizioni e le tracce implementano questa interfaccia.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interfaccia IAMTimelineSplittable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324265"
---
# <a name="iamtimelinesplittable-interface"></a>Interfaccia IAMTimelineSplittable

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineSplittable` interfaccia suddivide un oggetto sequenza temporale in [servizi di modifica DirectShow](directshow-editing-services.md) (des). Le origini, gli effetti, le transizioni e le tracce implementano questa interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineSplittable** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineSplittable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineSplittable** dispone di questi metodi.



| Metodo                                             | Descrizione                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | Suddivide l'oggetto all'ora specificata.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Suddivide l'oggetto all'ora specificata, specificato come valore [**REFTIME**](reftime.md) .<br/> |



 

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



 

 
