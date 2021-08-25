---
description: L'interfaccia IResize deve essere supportata da qualsiasi filtro di ridimensionamento video personalizzato per DirectShow Editing Services (DES). Per impostare un filtro di ridimensionamento personalizzato, chiamare il metodo IRenderEngine2::SetResizerGUID nel motore di rendering.
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interfaccia IResize (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 19aabd7c04cb5350ef3da87e1a20db6b75f6546f0fbcf5af3422c152bcafcf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818070"
---
# <a name="iresize-interface"></a>Interfaccia IResize

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`IResize`L'interfaccia deve essere supportata da qualsiasi filtro di ridimensionamento video personalizzato per DirectShow Editing Services (DES). Per impostare un filtro di ridimensionamento personalizzato, chiamare il metodo [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) nel motore di rendering.

## <a name="members"></a>Membri

**L'interfaccia IResize** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IResize** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IResize** include questi metodi.



| Metodo                                          | Descrizione                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**get \_ InputSize**](iresize-get-inputsize.md) | Restituisce le dimensioni di input correnti del filtro di ridimensionamento.<br/>  |
| [**get \_ MediaType**](iresize-get-mediatype.md) | Restituisce il tipo di supporto di output del filtro di ridimensionamento.<br/>   |
| [**get \_ Size**](iresize-get-size.md)           | Restituisce le dimensioni di output correnti e la modalità stretch.<br/> |
| [**put \_ MediaType**](iresize-put-mediatype.md) | Imposta il tipo di supporto di output.<br/>                       |
| [**Put \_ Size**](iresize-put-size.md)           | Imposta le dimensioni di output e la modalità stretch.<br/>            |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9.0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Fornire un ridimensionatore video personalizzato](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
