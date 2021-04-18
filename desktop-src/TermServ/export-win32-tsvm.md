---
title: Metodo Export della classe Win32_TSVm
description: Recupera le informazioni di monitoraggio della sessione della macchina virtuale.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Esporta il metodo Servizi Desktop remoto
- Metodo Export Servizi Desktop remoto, classe Win32_TSVm
- Classe Win32_TSVm Servizi Desktop remoto, metodo Export
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301230"
---
# <a name="export-method-of-the-win32_tsvm-class"></a>Metodo Export della classe Win32 \_ TSVm

Recupera le informazioni di monitoraggio della sessione della macchina virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ExportFolderPath* \[ in\]
</dt> <dd>

Percorso in cui verrà esportata la macchina virtuale.

</dd> <dt>

*ExportJobObjectPath* \[ out\]
</dt> <dd>

In seguito all'esito positivo restituisce il percorso dell'oggetto HyperV ConcreteJob.

</dd> </dl>

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

 

 





