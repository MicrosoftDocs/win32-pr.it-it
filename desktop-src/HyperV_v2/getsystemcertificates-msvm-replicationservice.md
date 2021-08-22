---
description: Recupera i certificati di sistema in un sistema host.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Metodo GetSystemCertificates della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bdc3fe1e2a12809dceb14a23e087d3e844f5e1a51401171b68dfe41303739c2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253621"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a>Metodo GetSystemCertificates della classe Msvm \_ ReplicationService

Recupera i certificati di sistema in un sistema host.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncodedCertificates* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, riceve i certificati disponibili dall'archivio personale per il computer locale. Ogni voce è una stringa di certificato con codifica Base 64. Questa stringa può essere convertita in una matrice di byte creando un oggetto X509Certificate2.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Operazione non** riuscita (32768)
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
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

 




