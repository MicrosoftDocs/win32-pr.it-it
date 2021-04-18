---
title: Metodo SetLoadBalancingState della classe Win32_TSSessionDirectory
description: Imposta il valore per indicare se il server parteciperà al bilanciamento del carico di Connessione Desktop remoto broker (gestore connessione Desktop remoto).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetLoadBalancingState
- Metodo SetLoadBalancingState Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetLoadBalancingState
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
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301293"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>Metodo SetLoadBalancingState della \_ classe TSSessionDirectory Win32

Imposta il valore per indicare se il server parteciperà al bilanciamento del carico di Connessione Desktop remoto broker (gestore connessione Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StateValue* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Indica se il server parteciperà al bilanciamento del carico di gestore connessione Desktop remoto.

<dt>

0
</dt> <dd>

Il server non parteciperà al bilanciamento del carico di gestore connessione Desktop remoto.

</dd> <dt>

1
</dt> <dd>

Il server parteciperà al bilanciamento del carico di gestore connessione Desktop remoto.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Il server deve essere aggiunto a una farm in Gestore connessione Desktop remoto.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

