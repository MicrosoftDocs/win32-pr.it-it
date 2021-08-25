---
title: Metodo SetLoadBalancingState della Win32_TSSessionDirectory classe
description: Imposta il valore per indicare se il server parteciperà Connessione Desktop remoto bilanciamento del carico di Gestore connessione Desktop remoto.
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Metodo SetLoadBalancingState Servizi Desktop remoto
- Metodo SetLoadBalancingState Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto, metodo SetLoadBalancingState
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d539f07c97e4e5b92152190a7bb38a8132d31a73daf08de8f140a39f67efdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987951"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>Metodo SetLoadBalancingState della classe \_ Win32 TSSessionDirectory

Imposta il valore per indicare se il server parteciperà Connessione Desktop remoto bilanciamento del carico di Gestore connessione Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StateValue* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Indica se il server parteciperà al bilanciamento del carico di Gestore connessione Desktop remoto.

<dt>

0
</dt> <dd>

Il server non parteciperà al bilanciamento del carico di Gestore connessione Desktop remoto.

</dd> <dt>

1
</dt> <dd>

Il server parteciperà al bilanciamento del carico di Gestore connessione Desktop remoto.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Il server deve essere aggiunto a una farm in Gestore connessione Desktop remoto.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

