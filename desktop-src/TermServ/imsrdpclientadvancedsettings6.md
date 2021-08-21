---
title: Interfaccia IMsRdpClientAdvancedSettings6
description: Espone le proprietà che gestiscono le impostazioni ActiveX controllo avanzate.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4c108345e3dae0b5c8f4e45c3a1c07299cccdaed44404718e599c0ef973957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352128"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a>Interfaccia IMsRdpClientAdvancedSettings6

Espone le proprietà che gestiscono le impostazioni ActiveX controllo avanzate. **L'interfaccia IMsRdpClientAdvancedSettings6** deriva dall'interfaccia [**IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md)

Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md) Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore **IMsTscAdvancedSettings** e passare **\_ IID IMsRdpClientAdvancedSettings6** a **QueryInterface**.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientAdvancedSettings6** eredita da [**IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md) **IMsRdpClientAdvancedSettings6** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IMsRdpClientAdvancedSettings6** ha queste proprietà.



| Proprietà                                                                                                  | Tipo di accesso           | Descrizione                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationServiceClass**](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | Lettura/Scrittura<br/> | Specifica il nome dell'entità servizio (SPN) da utilizzare per l'autenticazione al server.<br/>                                     |
| [**Authenticationtype**](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | Sola lettura<br/>  | Specifica il tipo di autenticazione utilizzato per la connessione.<br/>                                                          |
| [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | Lettura/Scrittura<br/> | Recupera o specifica se il controllo ActiveX deve tentare di connettersi al server per scopi amministrativi.<br/> |
| [**EnableCredSspSupport**](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | Lettura/Scrittura<br/> | Specifica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per questa connessione.<br/>                    |
| [**HotKeyFocusReleaseLeft**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | Lettura/Scrittura<br/> | Specifica il codice del tasto virtuale da aggiungere a CTRL+ALT per determinare la sostituzione del tasto di scelta rapida per CTRL+ALT+FRECCIA SINISTRA.<br/>          |
| [**HotKeyFocusReleaseRight**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | Lettura/Scrittura<br/> | Specifica il codice del tasto virtuale da aggiungere a CTRL+ALT per determinare la sostituzione del tasto di scelta rapida per CTRL+ALT+FRECCIA DESTRA.<br/>         |
| [**Pcb**](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | Lettura/Scrittura<br/> | Specifica l'impostazione DEL BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server.<br/>               |
| [**RelativeMouseMode**](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | Lettura/Scrittura<br/> | Specifica se il mouse deve utilizzare la modalità relativa.<br/>                                                                   |



 

## <a name="remarks"></a>Commenti

Questa interfaccia è stata estesa [**dall'interfaccia IMsRdpClientAdvancedSettings7,**](imsrdpclientadvancedsettings7.md) ereditando tutti i metodi e le proprietà delle interfacce precedenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

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

 

