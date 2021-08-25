---
title: Metodo MoveUp della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Sposta il criterio Desktop remoto di autorizzazione della connessione corrente (RD \ 160; CAP) una posizione in alto nell'ordine in cui RD \ 160; I CAP vengono valutati.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- Metodo MoveUp Servizi Desktop remoto
- Metodo MoveUp Servizi Desktop remoto , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto , metodo MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc5be4f15cee03097abcb52c50e3206d51872c8886970a49dbd20628f4b7beae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866371"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo MoveUp della classe \_ TSGatewayConnectionAuthorizationPolicy Win32

Sposta la posizione corrente Desktop remoto criteri di autorizzazione connessione Desktop remoto di una posizione verso l'alto nell'ordine in cui vengono valutati i criteri di autorizzazione connessioni Desktop remoto. Questo metodo decrementa la **proprietà Order** dell'oggetto CAP di Desktop remoto corrente e incrementa la proprietà **Order** dell'oggetto CAP di Desktop remoto che precedeva il cap di Desktop remoto corrente.

## <a name="syntax"></a>Sintassi


```mof
uint32 MoveUp();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

