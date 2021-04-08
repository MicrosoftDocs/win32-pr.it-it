---
title: Metodo DumpVmInfo della classe Win32_TSVm
description: Questo membro è a scopo di test interno e non deve essere utilizzato nel codice.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DumpVmInfo
- Metodo DumpVmInfo Servizi Desktop remoto, classe Win32_TSVm
- Classe Win32_TSVm Servizi Desktop remoto, metodo DumpVmInfo
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
ms.openlocfilehash: 1a2d02a1d4ea07bd045da2850a4d7ccb0069977a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743847"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a>Metodo DumpVmInfo della \_ classe TSVm Win32

Questo membro è a scopo di test interno e non deve essere utilizzato nel codice.

## <a name="syntax"></a>Sintassi


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSVm Win32**](win32-tsvm.md)
</dt> </dl>

 

 





