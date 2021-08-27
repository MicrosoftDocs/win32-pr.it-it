---
description: Verifica se la replica può essere abilitata dal sistema host corrente al sistema di ripristino specificato.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Metodo TestReplicationConnection della Msvm_ReplicationService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 729412ea2b506aedf09bcc77385c4c8b22d560d8cd8e6fc88b12c059c0bf049c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050381"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a>Metodo TestReplicationConnection della classe Msvm \_ ReplicationService

Verifica se la replica può essere abilitata dal sistema host corrente al sistema di ripristino specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RecoveryConnectionPoint* \[ Pollici\]
</dt> <dd>

Nome del punto di connessione. Per un cluster di ripristino, si tratta del nome CAP del broker. Per un server di ripristino autonomo, si tratta del nome del sistema host.

</dd> <dt>

*RecoveryServerPortNumber* \[ Pollici\]
</dt> <dd>

Numero di porta del punto di connessione di ripristino.

</dd> <dt>

*AuthenticationType* \[ Pollici\]
</dt> <dd>

Schema di autenticazione del ripristino. Deve essere uno dei valori seguenti.

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Autenticazione integrata** (1)


</dt> <dd>

Autenticazione Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticazione basata su certificati** (2)


</dt> <dd>

Autenticazione basata su certificati.

</dd> </dl> </dd> <dt>

*CertificateThumbPrint* \[ Pollici\]
</dt> <dd>

Identificazione personale del certificato da usare quando il *parametro AuthenticationType* è l'autenticazione basata su certificato.

</dd> <dt>

*BypassProxyServer* \[ Pollici\]
</dt> <dd>

Ignorare il server proxy durante la connessione al server di replica.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

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
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

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

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

