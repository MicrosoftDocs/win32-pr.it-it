---
title: Proprietà FullScreen IMsRdpClient
description: Determina se il controllo client è in modalità schermo intero.
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- Proprietà FullScreen Servizi Desktop remoto
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto , proprietà FullScreen
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto , proprietà FullScreen
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto , proprietà FullScreen
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , proprietà FullScreen
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , proprietà FullScreen
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto , proprietà FullScreen
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto , proprietà FullScreen
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto , proprietà FullScreen
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , proprietà FullScreen
- Proprietà FullScreen Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto , proprietà FullScreen
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e3d2349a4d3b0121b05a3a0424126b754757c1b0b356042a90c28ce9923ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010071"
---
# <a name="imsrdpclientfullscreen-property"></a>Proprietà IMsRdpClient::FullScreen

Determina se il controllo client è in modalità schermo intero.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a>Valore proprietà

**True** per accedere alla modalità schermo intero, **False** per uscire dalla modalità schermo intero e tornare alla modalità finestra.

## <a name="error-codes"></a>Codici di errore

Se i metodi hanno esito positivo, **viene restituito S \_ OK.** Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

È possibile impostare questa proprietà quando il controllo è connesso.

È necessario chiamare il metodo [**IMsRdpClientNonScriptable3::p ut \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) prima di chiamare il metodo [**\_ Fullscreen IMsTscSecuredSettings::p ut**](imstscsecuredsettings-fullscreen.md) o **IMsRdpClient::p ut \_ Fullscreen.**

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

 

 





