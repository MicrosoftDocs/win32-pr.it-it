---
title: Interfaccia IMsRdpClientAdvancedSettings7
description: Espone metodi e proprietà che gestiscono le impostazioni avanzate del controllo ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301223"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a>Interfaccia IMsRdpClientAdvancedSettings7

Espone metodi e proprietà che gestiscono le impostazioni avanzate del controllo ActiveX.

Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore **IMsTscAdvancedSettings** e passare **IID \_ IMsRdpClientAdvancedSettings7** a **QueryInterface**.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientAdvancedSettings7** eredita da **IMsRdpClientAdvancedSettings6**. **IMsRdpClientAdvancedSettings7** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientAdvancedSettings7** ha queste proprietà.



| Proprietà                                                                                                    | Tipo di accesso           | Descrizione                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AudioCaptureRedirectionMode**](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | Lettura/Scrittura<br/> | Specifica o recupera un valore che indica se il dispositivo di input audio predefinito viene reindirizzato dal client alla sessione remota.<br/> |
| [**AudioQualityMode**](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | Lettura/Scrittura<br/> | Specifica o recupera un valore che indica l'impostazione della modalità di qualità audio per l'audio reindirizzato.<br/>                                        |
| [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | Lettura/Scrittura<br/> | Specifica o recupera un valore che indica se SuperPan è abilitato o disabilitato.<br/>                                                    |
| [**NetworkConnectionType**](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | Lettura/Scrittura<br/> | Specifica o recupera un valore che indica il tipo di connessione di rete.<br/>                                                                |
| [**RedirectDirectX**](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | Lettura/Scrittura<br/> | Questa proprietà non viene utilizzata.<br/>                                                                                                                |
| [**SuperPanAccelerationFactor**](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | Lettura/Scrittura<br/> | Specifica o recupera un valore che indica il fattore di accelerazione SuperPan.<br/>                                                           |
| [**VideoPlaybackMode**](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | Lettura/Scrittura<br/> | Specifica o recupera un valore che indica la modalità di riproduzione video.<br/>                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                             |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

