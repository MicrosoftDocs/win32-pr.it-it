---
description: L'interfaccia IWiaUIExtension fornisce metodi che sostituiscono l'interfaccia utente di sistema predefinita, forniscono un logo bitmap personalizzato del dispositivo e forniscono un'icona personalizzata del dispositivo.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Interfaccia IWiaUIExtension (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307346"
---
# <a name="iwiauiextension-interface"></a>Interfaccia IWiaUIExtension

L'interfaccia **IWiaUIExtension** fornisce metodi che sostituiscono l'interfaccia utente di sistema predefinita, forniscono un logo bitmap personalizzato del dispositivo e forniscono un'icona personalizzata del dispositivo.

## <a name="members"></a>Membri

L'interfaccia **IWiaUIExtension** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaUIExtension** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWiaUIExtension** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension-devicedialog.md)               | Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.<br/> |
| [**GetDeviceBitmapLogo**](-wia-iwiauiextension-getdevicebitmaplogo.md) | Ottiene un logo bitmap personalizzato per il dispositivo.<br/>                                         |
| [**GetDeviceIcon**](-wia-iwiauiextension-getdeviceicon.md)             | Ottiene un'icona di dispositivo personalizzata.<br/>                                                        |



 

## <a name="remarks"></a>Commenti



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 
