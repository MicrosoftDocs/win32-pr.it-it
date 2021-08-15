---
description: L'interfaccia IWiaUIExtension2 fornisce metodi che sostituiscono l'interfaccia utente predefinita fornita dal sistema con un'interfaccia utente personalizzata e che forniscono un'icona del dispositivo personalizzata.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interfaccia IWiaUIExtension2 (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 2111c25a83a9b826f4cab7dba8f689e01a9868ac416b8fb3026f1b1fb49a90ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208144"
---
# <a name="iwiauiextension2-interface"></a>Interfaccia IWiaUIExtension2

L'interfaccia IWiaUIExtension2 fornisce metodi che sostituiscono l'interfaccia utente predefinita fornita dal sistema con un'interfaccia utente personalizzata e che forniscono un'icona del dispositivo personalizzata. I fornitori di dispositivi possono implementare questa interfaccia per fornire interfacce utente personalizzate per i dispositivi.

## <a name="members"></a>Membri

**L'interfaccia IWiaUIExtension2** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaUIExtension2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWiaUIExtension2** include questi metodi.



| Metodo                                                       | Descrizione                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Finestra di dialogo Dispositivo**](-wia-iwiauiextension2-devicedialog.md)   | Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.<br/> |
| [**GetDeviceIcon**](-wia-iwiauiextension2-getdeviceicon.md) | Ottiene un'icona del dispositivo personalizzata.<br/>                                                        |



 

## <a name="remarks"></a>Commenti



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 
