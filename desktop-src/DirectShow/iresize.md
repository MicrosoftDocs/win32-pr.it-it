---
description: "L'interfaccia IResize deve essere supportata da qualsiasi filtro di ridimensionamento video personalizzato per i servizi di modifica DirectShow (DES). Per impostare un filtro Resizer personalizzato, chiamare il metodo IRenderEngine2:: SetResizerGUID sul motore di rendering."
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interfaccia IResize (qedit. h)
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
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325298"
---
# <a name="iresize-interface"></a>Interfaccia IResize

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IResize` interfaccia deve essere supportata da qualsiasi filtro di ridimensionamento video personalizzato per i servizi di modifica DirectShow (des). Per impostare un filtro Resizer personalizzato, chiamare il metodo [**IRenderEngine2:: SetResizerGUID**](irenderengine2-setresizerguid.md) sul motore di rendering.

## <a name="members"></a>Membri

L'interfaccia **IResize** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IResize** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IResize** dispone di questi metodi.



| Metodo                                          | Descrizione                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**ottenere \_ InputSize**](iresize-get-inputsize.md) | Restituisce le dimensioni di input correnti del filtro Resizer.<br/>  |
| [**ottenere \_ mediaType**](iresize-get-mediatype.md) | Restituisce il tipo di supporto di output del filtro di ridimensionamento.<br/>   |
| [**Ottieni \_ dimensioni**](iresize-get-size.md)           | Restituisce le dimensioni di output e la modalità di estensione correnti.<br/> |
| [**Inserisci \_ mediaType**](iresize-put-mediatype.md) | Imposta il tipo di supporto di output.<br/>                       |
| [**\_dimensioni put**](iresize-put-size.md)           | Imposta le dimensioni di output e la modalità di estensione.<br/>            |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9,0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Creazione di una ridisposizione video personalizzata](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
