---
title: Proprietà IMsRdpClient7 SecuredSettings3
description: Recupera un oggetto che supporta l'interfaccia IMsRdpClientSecuredSettings2.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- Proprietà SecuredSettings3 Servizi Desktop remoto
- Proprietà SecuredSettings3 Servizi Desktop remoto , interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto , proprietà SecuredSettings3
- Proprietà SecuredSettings3 Servizi Desktop remoto , interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto , proprietà SecuredSettings3
- Proprietà SecuredSettings3 Servizi Desktop remoto , interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , proprietà SecuredSettings3
- Proprietà SecuredSettings3 Servizi Desktop remoto , interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto , proprietà SecuredSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77bcdaae672ca59c65bea46d97a34046c7e48c6f0964c1a5b97cdcef77c14ffd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737171"
---
# <a name="imsrdpclient7securedsettings3-property"></a>Proprietà IMsRdpClient7::SecuredSettings3

Recupera un oggetto che supporta [**l'interfaccia IMsRdpClientSecuredSettings2.**](imsrdpclientsecuredsettings2.md)

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a>Valore proprietà

Indirizzo di un puntatore a interfaccia [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) che riceve l'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClient7 IID è definito come \_ b2a5b5ce-3461-444a-91d4-add26d070638<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





