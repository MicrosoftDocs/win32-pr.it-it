---
title: Proprietà AdvancedSettings4 di IMsRdpClient3
description: Recupera un puntatore all'interfaccia IMsRdpClientAdvancedSettings3.
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a229c28b645e7920212a04cc44ca5a9ce42be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873449"
---
# <a name="imsrdpclient3advancedsettings4-property"></a>Proprietà IMsRdpClient3:: AdvancedSettings4

Recupera un puntatore all'interfaccia [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore all'interfaccia [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) . L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, viene restituito **S \_ OK** . Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

Impossibile impostare questa proprietà quando il controllo è connesso.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient3 è definito come 91b7cbc5-a72e-4fa0-9300-d647d7e897ff<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

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

 

 





