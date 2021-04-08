---
description: Fornisce la funzionalità per ottenere IMFDXGIDeviceManager dall'Microsoft Media Foundation sink di rendering video.
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: Interfaccia IMFDXGIDeviceManagerSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 669ec840a3122172147840052bd1dbf5c940569d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753191"
---
# <a name="imfdxgidevicemanagersource-interface"></a>Interfaccia IMFDXGIDeviceManagerSource

Fornisce la funzionalità per ottenere [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) dall'Microsoft Media Foundation sink di rendering video.

## <a name="members"></a>Membri

L'interfaccia **IMFDXGIDeviceManagerSource** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMFDXGIDeviceManagerSource** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMFDXGIDeviceManagerSource** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [**GetManager**](imfdxgidevicemanagersource-getmanager.md) | Ottiene [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) dal sink di rendering del video Media Foundation.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Media Foundation](media-foundation-interfaces.md)
</dt> </dl>

 

 
