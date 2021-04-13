---
title: Proprietà shutdownTimeout di IMsRdpClientAdvancedSettings
description: Specifica il tempo di attesa, in secondi, per la risposta del server a una richiesta di disconnessione.
ms.assetid: 3fa935dc-d4b0-433b-ab67-a644fcf09006
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà shutdownTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.shutdownTimeout
- IMsRdpClientAdvancedSettings.get_shutdownTimeout
- IMsRdpClientAdvancedSettings.put_shutdownTimeout
- IMsRdpClientAdvancedSettings2.shutdownTimeout
- IMsRdpClientAdvancedSettings2.get_shutdownTimeout
- IMsRdpClientAdvancedSettings2.put_shutdownTimeout
- IMsRdpClientAdvancedSettings3.shutdownTimeout
- IMsRdpClientAdvancedSettings3.get_shutdownTimeout
- IMsRdpClientAdvancedSettings3.put_shutdownTimeout
- IMsRdpClientAdvancedSettings4.shutdownTimeout
- IMsRdpClientAdvancedSettings4.get_shutdownTimeout
- IMsRdpClientAdvancedSettings4.put_shutdownTimeout
- IMsRdpClientAdvancedSettings5.shutdownTimeout
- IMsRdpClientAdvancedSettings5.get_shutdownTimeout
- IMsRdpClientAdvancedSettings5.put_shutdownTimeout
- IMsRdpClientAdvancedSettings6.shutdownTimeout
- IMsRdpClientAdvancedSettings6.get_shutdownTimeout
- IMsRdpClientAdvancedSettings6.put_shutdownTimeout
- IMsRdpClientAdvancedSettings7.shutdownTimeout
- IMsRdpClientAdvancedSettings7.get_shutdownTimeout
- IMsRdpClientAdvancedSettings7.put_shutdownTimeout
- IMsRdpClientAdvancedSettings8.shutdownTimeout
- IMsRdpClientAdvancedSettings8.get_shutdownTimeout
- IMsRdpClientAdvancedSettings8.put_shutdownTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a011a0ce484f5bb2dd7d1ec610f4e3a436898
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400242"
---
# <a name="imsrdpclientadvancedsettingsshutdowntimeout-property"></a>Proprietà IMsRdpClientAdvancedSettings:: shutdownTimeout

Specifica il tempo di attesa, in secondi, per la risposta del server a una richiesta di disconnessione.

Se il server non risponde entro il tempo specificato, il controllo client si disconnette.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_shutdownTimeout(
  [in]  LONG shutdownTimeout
);

HRESULT get_shutdownTimeout(
  [out] LONG *pshutdownTimeout
);
```



## <a name="property-value"></a>Valore proprietà

Nuova ora, in secondi. Il valore predefinito della proprietà è 10. Il valore massimo è 600, che rappresenta 10 minuti.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                        |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                  |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





