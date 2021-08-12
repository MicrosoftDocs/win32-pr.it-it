---
description: Recupera le dimensioni correnti, in byte, dello spazio degli indirizzi virtuali disponibile per il processo.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Metodo GetAvailableVirtualSize della Win32_Process classe
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
ms.openlocfilehash: 7cdea363ce835297469242a4166d5e1e9eeea0845f27d0c780eef88f775bf751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675993"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a>Metodo GetAvailableVirtualSize della classe Win32 \_ Process

Recupera le dimensioni correnti, in byte, dello spazio degli indirizzi virtuali disponibile per il processo.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AvailableVirtualSize* \[ Cambio\]
</dt> <dd>

Il *parametro AvailableVirtualSize* restituisce lo spazio degli indirizzi virtuali disponibile per questo processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

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

**Privilegi insufficienti**
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

Per valori diversi da quelli elencati, vedere la documentazione [relativa ai codici di errore di](/windows/desktop/Debug/system-error-codes) sistema.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                       |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo \_ Win32**](win32-process.md)
</dt> </dl>

 

