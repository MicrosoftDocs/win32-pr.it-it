---
description: Restituisce una stringa del messaggio di errore formattato per la matrice specificata di istanze di errore MSVM incorporate \_ .
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
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307759"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo FormatError della classe MSVM \_ VirtualSystemManagementService

Restituisce una stringa del messaggio di errore formattato per la matrice specificata di istanze di [**\_ errore MSVM**](msvm-error.md) incorporate.

## <a name="syntax"></a>Sintassi


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errori* \[ di in\]
</dt> <dd>

Tipo: **stringa \[ \]**

Matrice di stringhe contenente le istanze di [**\_ errore MSVM**](msvm-error.md) utilizzate per generare il messaggio di errore di output.

</dd> <dt>

*ErrorMessage* \[ out\]
</dt> <dd>

Tipo: **stringa**

Nell'output, stringa che contiene i messaggi di errore concatenati rappresentati dalle istanze di [**\_ errore MSVM**](msvm-error.md) passate nel parametro *Errors* . Ogni stringa di errore è separata da una coppia di caratteri di nuova riga (' \\ n').

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

Il **sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FormatError (V1)**](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

