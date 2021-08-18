---
title: Interfaccia IMsRdpClientAdvancedSettings2
description: Gestisce le impostazioni client avanzate. Deriva dall'interfaccia IMsRdpClientAdvancedSettings.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97584aa3b37adc148672777e95fe0b2c8b101e09989bfa1ab5debbffe489640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001409"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a>Interfaccia IMsRdpClientAdvancedSettings2

Gestisce le impostazioni client avanzate. Deriva [**dall'interfaccia IMsRdpClientAdvancedSettings.**](imsrdpclientadvancedsettings-interface.md) Questa interfaccia include metodi per recuperare e impostare proprietà avanzate (facoltative) per il Desktop remoto ActiveX controllo.

Per ottenere un'istanza di questa interfaccia, usare la [**proprietà IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md) Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul **puntatore IMsTscAdvancedSettings** e passare **\_ IMsRdpClientAdvancedSettings2** a **QueryInterface**.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientAdvancedSettings2** eredita da [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md). **IMsRdpClientAdvancedSettings2** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IMsRdpClientAdvancedSettings2.**



| Proprietà                                                                                      | Tipo di accesso           | Descrizione                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutoReconnect**](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | Sola lettura<br/>  | Specifica se il controllo client è in grado di riconnettersi automaticamente alla sessione corrente in caso di disconnessione di rete.<br/>    |
| [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | Lettura/Scrittura<br/> | Specifica se consentire al controllo client di riconnettersi automaticamente a una sessione in caso di disconnessione di rete.<br/>            |
| [**MaxReconnectAttempts**](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | Lettura/Scrittura<br/> | Specifica il numero di volte in cui provare a riconnettersi durante la riconnessione automatica. I valori validi di questa proprietà sono compresi tra 0 e 200 inclusi.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia è stata estesa dalle interfacce seguenti, con ogni nuova interfaccia che eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 è definito come 9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Connessione Web Desktop remoto riferimento](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

