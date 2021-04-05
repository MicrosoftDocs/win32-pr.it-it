---
title: Interfaccia IMsRdpClientAdvancedSettings3
description: Gestisce le impostazioni client avanzate. Deriva dall'interfaccia IMsRdpClientAdvancedSettings2.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760ae7d40742a800556b3d62bc5a1609b89c986b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741346"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a>Interfaccia IMsRdpClientAdvancedSettings3

Gestisce le impostazioni client avanzate. Deriva dall'interfaccia [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . Questa interfaccia include metodi per recuperare e impostare proprietà avanzate (facoltative) per il controllo ActiveX Desktop remoto.

Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore **IMsTscAdvancedSettings** e passare **IID \_ IMsRdpClientAdvancedSettings3** a **QueryInterface**.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientAdvancedSettings3** eredita da [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md). **IMsRdpClientAdvancedSettings3** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientAdvancedSettings3** ha queste proprietà.



| Proprietà                                                                                                            | Tipo di accesso           | Descrizione                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [**ConnectionBarShowMinimizeButton**](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | Lettura/Scrittura<br/> | Specifica se visualizzare il pulsante **Riduci a icona** sulla barra delle connessioni.<br/> |
| [**ConnectionBarShowRestoreButton**](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | Lettura/Scrittura<br/> | Specifica se visualizzare il pulsante **Ripristina** sulla barra delle connessioni.<br/>  |



 

## <a name="remarks"></a>Commenti

Questa interfaccia è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 è definito come 19cd856b-C542-4c53-Acee-f127e3be1a59<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

