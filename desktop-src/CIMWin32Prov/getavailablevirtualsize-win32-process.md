---
description: Recupera le dimensioni correnti, in byte, dello spazio degli indirizzi virtuali libero disponibile per il processo.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Metodo GetAvailableVirtualSize della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304689"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a>Metodo GetAvailableVirtualSize della classe di \_ processo Win32

Recupera le dimensioni correnti, in byte, dello spazio degli indirizzi virtuali libero disponibile per il processo.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AvailableVirtualSize* \[ out\]
</dt> <dd>

Il parametro *AvailableVirtualSize* restituisce lo spazio degli indirizzi virtuali libero disponibile per questo processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione completata**
</dt> <dd>

0

Operazione riuscita.

</dd> <dt>

**Accesso negato**
</dt> <dd>

2

L'utente non ha accesso alle informazioni richieste

</dd> <dt>

**Privilegio insufficiente**
</dt> <dd>

3

L'utente non dispone di privilegi sufficienti.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

8

Errore sconosciuto.

</dd> <dt>

**Impossibile trovare il percorso**
</dt> <dd>

9

Il percorso specificato non esiste.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

21

Il parametro specificato non è valido.

</dd> <dt>

**Altri**
</dt> <dd>

22 4294967295

Per i valori diversi da quelli elencati, fare riferimento alla documentazione relativa ai [codici di errore di sistema](/windows/desktop/Debug/system-error-codes) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                       |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> </dl>

 

