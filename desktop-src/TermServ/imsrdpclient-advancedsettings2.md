---
title: Proprietà AdvancedSettings2 di IMsRdpClient
description: Recupera un puntatore all'interfaccia IMsRdpClientAdvancedSettings. L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.
ms.assetid: 207b625c-fc2b-41ad-9339-9f3c3b8eeab7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings2
- Servizi Desktop remoto proprietà AdvancedSettings2, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.AdvancedSettings2
- IMsRdpClient.get_AdvancedSettings2
- IMsRdpClient2.AdvancedSettings2
- IMsRdpClient2.get_AdvancedSettings2
- IMsRdpClient3.AdvancedSettings2
- IMsRdpClient3.get_AdvancedSettings2
- IMsRdpClient4.AdvancedSettings2
- IMsRdpClient4.get_AdvancedSettings2
- IMsRdpClient5.AdvancedSettings2
- IMsRdpClient5.get_AdvancedSettings2
- IMsRdpClient6.AdvancedSettings2
- IMsRdpClient6.get_AdvancedSettings2
- IMsRdpClient7.AdvancedSettings2
- IMsRdpClient7.get_AdvancedSettings2
- IMsRdpClient8.AdvancedSettings2
- IMsRdpClient8.get_AdvancedSettings2
- IMsRdpClient9.AdvancedSettings2
- IMsRdpClient9.get_AdvancedSettings2
- IMsRdpClient10.AdvancedSettings2
- IMsRdpClient10.get_AdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683d56d5e9501114b1e60635ca406b4509d2032b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302470"
---
# <a name="imsrdpclientadvancedsettings2-property"></a>Proprietà IMsRdpClient:: AdvancedSettings2

Recupera un puntatore all'interfaccia [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) . L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AdvancedSettings2(
  [out] IMsRdpClientAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore all'interfaccia [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) . L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, viene restituito **S \_ OK** . Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a<br/>        |



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

 

 





