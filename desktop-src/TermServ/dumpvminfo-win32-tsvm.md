---
title: Metodo DumpVmInfo della classe Win32_TSVm
description: Questo membro è a scopo di test interno e non deve essere usato nel codice.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Metodo DumpVmInfo Servizi Desktop remoto
- Il metodo DumpVmInfo Servizi Desktop remoto , Win32_TSVm classe
- Win32_TSVm classe Servizi Desktop remoto , metodo DumpVmInfo
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c74602e09f7aab4909e78bcd4696a450419e929b89769b35e16f21cbcafc080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354022"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a>Metodo DumpVmInfo della classe TSVm Win32 \_

Questo membro è a scopo di test interno e non deve essere usato nel codice.

## <a name="syntax"></a>Sintassi


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSVm**](win32-tsvm.md)
</dt> </dl>

 

 





