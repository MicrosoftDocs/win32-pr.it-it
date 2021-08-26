---
description: L'interfaccia IAMTimelineSplittable suddivide un oggetto sequenza temporale in DirectShow Editing Services (DES). Origini, effetti, transizioni e tracce implementano questa interfaccia.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interfaccia IAMTimelineSplittable (Qedit.h)
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
ms.openlocfilehash: fd9f3ca6b1bdea5f80c117b869163d9a2375d5b434765b5962c6216795dd9e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078971"
---
# <a name="iamtimelinesplittable-interface"></a>Interfaccia IAMTimelineSplittable

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`IAMTimelineSplittable`L'interfaccia suddivide un oggetto sequenza temporale in DirectShow Editing [Services](directshow-editing-services.md) (DES). Origini, effetti, transizioni e tracce implementano questa interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IAMTimelineSplittable** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineSplittable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IAMTimelineSplittable.**



| Metodo                                             | Descrizione                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | Divide l'oggetto all'ora specificata.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Suddivide l'oggetto all'ora specificata, specificato come [**valore REFTIME.**](reftime.md)<br/> |



 

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



 

 
