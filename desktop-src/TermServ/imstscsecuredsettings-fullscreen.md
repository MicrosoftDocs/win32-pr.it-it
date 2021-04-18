---
title: Proprietà IMsTscSecuredSettings fullscreen
description: Specifica lo stato a schermo intero del controllo client.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà a schermo intero
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsTscSecuredSettings
- Interfaccia IMsTscSecuredSettings Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, proprietà FullScreen
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302458"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a>Proprietà IMsTscSecuredSettings:: fullscreen

Specifica lo stato a schermo intero del controllo client.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su **true** se il controllo deve utilizzare la modalità a schermo intero e **false** in caso contrario.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su questo metodo, vedere la pagina [relativa alla sicurezza dei client RDP](providing-for-rdp-client-security.md).

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

Si noti che anche se l'uso di questa proprietà è limitato alle zone di sicurezza URL di Internet Explorer consentite, un utente può sempre passare alla modalità schermo intero dopo che la connessione è stata stabilita premendo la combinazione di [tasti di scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).

Questo metodo può essere chiamato mentre viene stabilita la connessione client.

È necessario chiamare il metodo [**IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) prima di chiamare il metodo **IMsTscSecuredSettings::P UT \_ FullScreen** o [**IMsRdpClient::p UT \_ FullScreen**](imsrdpclient-fullscreen.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings è definito come c9d65442-A0F9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





