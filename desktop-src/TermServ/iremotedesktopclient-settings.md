---
title: Proprietà delle impostazioni IRemoteDesktopClient
description: Recupera l'oggetto impostazioni per il client contenitore di app Remote Desktop Protocol (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà Settings
- Servizi Desktop remoto delle proprietà Settings, interfaccia IRemoteDesktopClient
- Servizi Desktop remoto di interfaccia IRemoteDesktopClient, proprietà Settings
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964504"
---
# <a name="iremotedesktopclientsettings-property"></a>Proprietà IRemoteDesktopClient:: Settings

Recupera l'oggetto impostazioni per il client contenitore di app Remote Desktop Protocol (RDP).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a>Valore proprietà

Oggetto impostazioni per il client RDP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IRemoteDesktopClient è definito come 57D25668-625A-4905-BE4E-304CAA13F89C<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

