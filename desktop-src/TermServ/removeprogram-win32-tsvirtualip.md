---
title: Metodo RemoveProgram della classe Win32_TSVirtualIP (Bdaiface. h)
description: Rimuove un programma dall'elenco di programmi che utilizzano la virtualizzazione IP.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveProgram
- Metodo RemoveProgram Servizi Desktop remoto, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Servizi Desktop remoto, metodo RemoveProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743626"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a>Metodo RemoveProgram della \_ classe TSVirtualIP Win32

Rimuove un programma dall'elenco di programmi che utilizzano la virtualizzazione IP.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProgramPath* \[ in\]
</dt> <dd>

Tipo: **stringa**

Percorso e nome file del programma da rimuovere dall'elenco. Se il programma non viene trovato, viene restituito un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Bdaiface. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





