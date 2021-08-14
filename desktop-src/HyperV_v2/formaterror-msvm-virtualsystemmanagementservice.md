---
description: Restituisce una stringa di messaggio di errore formattata per la matrice specificata di istanze di Msvm \_ Error incorporate.
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Metodo FormatError della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31b7f2ba03c21c08af3b9249c0ee3099291fdd190d22516ed503c012dae63f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253951"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo FormatError della classe Msvm \_ VirtualSystemManagementService

Restituisce una stringa di messaggio di errore formattata per la matrice specificata di [**istanze di Msvm \_ Error**](msvm-error.md) incorporate.

## <a name="syntax"></a>Sintassi


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errori* \[ Pollici\]
</dt> <dd>

Tipo: **\[ \] string**

Matrice di stringhe contenente le [**istanze di Msvm \_ Error**](msvm-error.md) usate per generare il messaggio di errore di output.

</dd> <dt>

*Messaggio di errore* \[ Cambio\]
</dt> <dd>

Tipo: **string**

Nell'output, stringa che contiene i messaggi di errore concatenati rappresentati dalle [**istanze di Msvm \_ Error**](msvm-error.md) passate nel *parametro Errors.* Ogni stringa di errore è separata da una coppia di caratteri di nuova riga (' \\ n').

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Il sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FormatError (V1)**](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

