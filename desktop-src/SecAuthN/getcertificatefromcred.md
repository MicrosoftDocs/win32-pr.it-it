---
description: Ottiene il certificato dalle credenziali utente.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Funzione GetCertificateFromCred (Lsaidprov.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 3660fd4cfb8baa3e025789a2cde9dc04dd7e1e1678b0516a56562f1ea5be43dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994482"
---
# <a name="getcertificatefromcred-function"></a>Funzione GetCertificateFromCred

Ottiene il certificato dalle credenziali utente.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProviderHandle* \[ Pollici\]
</dt> <dd>

Handle del provider di identità.

</dd> <dt>

*ClientToken* \[ Pollici\]
</dt> <dd>

Token del chiamante che sta recuperando il certificato.

</dd> <dt>

*SuppliedCred* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura SECPKG \_ SUPPLIED \_ CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) che contiene le credenziali di un ID online il cui certificato è richiesto. Il provider di identità deve convalidare i dati di input come se proviene da un'origine non attendibile.

</dd> <dt>

*SuppliedCredSize* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *SuppliedCred.*

</dd> <dt>

*CertContext* \[ Cambio\]
</dt> <dd>

Se la funzione ha esito positivo, questo parametro è un puntatore al puntatore CCERT \_ CONTEXT restituito. Al termine dell'uso del contesto del certificato, rilasciarlo chiamando la funzione [**CertFreeCertificateContext.**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce STATUS \_ SUCCESS.

Se la funzione ha esito negativo, la funzione può restituire uno dei codici di errore NTSTATUS seguenti.



| Valore restituito                                                                                            | Descrizione                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>STATO \_ NON \_ SUPPORTATO</dt> </dl>       | Il provider di identità non riconosce il tipo di credenziale della credenziale fornita. LSA tenterà il provider di identità successivo.<br/>                                           |
| <dl> <dt>ERRORE \_ DI ACCESSO ALLO \_ STATO</dt> </dl>       | La credenziale non è corretta.<br/>                                                                                                                                                |
| <dl> <dt>STATO \_ PARAMETRO NON \_ VALIDO</dt> </dl>   | Un parametro non è valido. La credenziale potrebbe essere in un formato non corretto e non nella struttura [**SECPKG \_ SUPPLIED \_ CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) definita.<br/> |
| <dl> <dt>RETE \_ DI STATO NON \_ RAGGIUNGIBILE</dt> </dl> | Il provider di identità non può contattare il cloud per ottenere il certificato.<br/>                                                                                                   |
| <dl> <dt>PASSWORD \_ DI STATO \_ SCADUTA</dt> </dl>    | La password dell'account è scaduta.<br/>                                                                                                                                           |
| <dl> <dt>ACCOUNT \_ DI STATO \_ \_ BLOCCATO</dt> </dl> | L'account è stato bloccato. <br/>                                                                                                                                           |
| <dl> <dt>Altro</dt> </dl>                       | Altri codici di errore specifici del provider. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Prima di recuperare il certificato dal cloud, il provider di identità deve verificare che sia presente un certificato valido per questo utente nell'archivio certificati "MY" dell'utente. Se esiste un certificato valido, il provider deve restituire questo certificato per evitare traffico di rete non necessario.

Il provider di identità può anche memorizzare il certificato nella cache locale, purché sia protetto dall'utente corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Lsaidprov.h</dt> </dl> |



 

