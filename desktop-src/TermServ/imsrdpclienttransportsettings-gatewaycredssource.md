---
title: Proprietà GatewayCredsSource di IMsRdpClientTransportSettings
description: Specifica o Recupera il metodo di autenticazione del Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayCredsSource
- Servizi Desktop remoto proprietà GatewayCredsSource, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400382"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a>Proprietà IMsRdpClientTransportSettings:: GatewayCredsSource

Specifica o Recupera il metodo di autenticazione del Gateway Desktop remoto (Gateway Desktop remoto).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Valore proprietà

Variabile **ULONG** che specifica il metodo di autenticazione Gateway Desktop remoto. Questo parametro può avere uno dei valori seguenti.

<dt>

\_Modalità credenziali del proxy TSC \_ \_ \_ USERPASS (0)
</dt> <dd>

Usare una password (NTLM) come metodo di autenticazione per Gateway Desktop remoto.

</dd> <dt>

\_ \_ Smart Card della modalità credenziali del proxy TSC \_ \_ (1)
</dt> <dd>

Usare una smart card come metodo di autenticazione per Gateway Desktop remoto.

</dd> <dt>

\_Modalità credenziali del proxy TSC \_ \_ \_ Any (4)
</dt> <dd>

Usare qualsiasi metodo di autenticazione per Gateway Desktop remoto.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





