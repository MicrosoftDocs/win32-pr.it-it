---
title: Proprietà IMsRdpClient SecuredSettings2
description: Recupera un puntatore all'interfaccia IMsRdpClientSecuredSettings. Questa interfaccia può essere usata per impostare le impostazioni protette per il controllo client.
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- Proprietà SecuredSettings2 Servizi Desktop remoto
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto , proprietà SecuredSettings2
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto , proprietà SecuredSettings2
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto , proprietà SecuredSettings2
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , proprietà SecuredSettings2
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , proprietà SecuredSettings2
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto , proprietà SecuredSettings2
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto , proprietà SecuredSettings2
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto , proprietà SecuredSettings2
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , proprietà SecuredSettings2
- Proprietà SecuredSettings2 Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto , proprietà SecuredSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0dff321eed8da198cafeb2fd58cf37661f100b08fbc52ac7c90be9c2575c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771781"
---
# <a name="imsrdpclientsecuredsettings2-property"></a>Proprietà IMsRdpClient::SecuredSettings2

Recupera un puntatore [**all'interfaccia IMsRdpClientSecuredSettings.**](imsrdpclientsecuredsettings-interface.md) Questa interfaccia può essere usata per impostare le impostazioni protette per il controllo client.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore [**a interfaccia IMsRdpClientSecuredSettings.**](imsrdpclientsecuredsettings-interface.md)

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, **viene restituito S \_ OK.** Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

Per altre informazioni, vedere [**l'interfaccia IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) e [Providing for RDP Client Security](providing-for-rdp-client-security.md).

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClient IID è definito come \_ 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





