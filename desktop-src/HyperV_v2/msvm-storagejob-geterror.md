---
description: "Metodo GetError della classe Msvm_StorageJob: recupera l'errore."
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Metodo GetError della classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 00434ef529b7f26755f52833ff6f37310c7dc210
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109599"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a>Metodo GetError della classe Msvm \_ StorageJob

Recupera l'errore.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errore* \[ Cambio\]
</dt> <dd>

Errore recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Completata senza errori** (0)
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

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo di \_ archiviazione Msvm**](msvm-storagejob.md)
</dt> </dl>

 

 




