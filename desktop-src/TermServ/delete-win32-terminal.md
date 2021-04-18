---
title: Metodo Delete della classe Win32_Terminal
description: Elimina il terminale specificato.
ms.assetid: 59d8cc73-aef1-49d2-a7a2-dd3cbe5a8c52
ms.tgt_platform: multiple
keywords:
- Elimina Servizi Desktop remoto del metodo
- Metodo Delete Servizi Desktop remoto, classe Win32_Terminal
- Classe Win32_Terminal Servizi Desktop remoto, metodo Delete
topic_type:
- apiref
api_name:
- Win32_Terminal.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b7120c78eada2b047f836219d3382e5ce1e2f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301127"
---
# <a name="delete-method-of-the-win32_terminal-class"></a>Metodo Delete della \_ classe terminale Win32

Il metodo **Delete** Elimina il terminale specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 Delete(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewTerminalName* \[ in\]
</dt> <dd>

Nome del terminale da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Terminale Win32**](win32-terminal.md)
</dt> </dl>

 

