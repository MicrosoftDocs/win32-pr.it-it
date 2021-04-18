---
title: Proprietà EnableAutoReconnect di IMsRdpClientAdvancedSettings2
description: Specifica se abilitare il controllo client per la riconnessione automatica a una sessione in caso di disconnessione di rete.
ms.assetid: 9d820f78-bf7f-479a-ae6f-be0f0abe549c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà EnableAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.put_EnableAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8d4a1345395b5b5843872df256fe7a113094e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301993"
---
# <a name="imsrdpclientadvancedsettings2enableautoreconnect-property"></a>Proprietà IMsRdpClientAdvancedSettings2:: EnableAutoReconnect

Specifica se abilitare il controllo client per la riconnessione automatica a una sessione in caso di disconnessione di rete.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_EnableAutoReconnect(
  [in]  VARIANT_BOOL fEnableAutoReconnect
);

HRESULT get_EnableAutoReconnect(
  [out] VARIANT_BOOL *pfEnableAutoReconnect
);
```



## <a name="property-value"></a>Valore proprietà

Impostare su **Variant \_ true** per abilitare la riconnessione automatica e su **Variant \_ false** per disabilitarla. Il valore predefinito è **Variant \_ true**.

## <a name="error-codes"></a>Codici di errore

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Impossibile impostare questa proprietà quando il controllo è connesso.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 è definito come 9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

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

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





