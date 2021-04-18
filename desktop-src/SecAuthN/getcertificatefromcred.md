---
description: Ottiene il certificato dalle credenziali dell'utente.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Funzione GetCertificateFromCred (Lsaidprov. h)
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
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310475"
---
# <a name="getcertificatefromcred-function"></a>GetCertificateFromCred (funzione)

Ottiene il certificato dalle credenziali dell'utente.

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

*ProviderHandle* \[ in\]
</dt> <dd>

Handle del provider di identità.

</dd> <dt>

*ClientToken* \[ in\]
</dt> <dd>

Token del chiamante che sta recuperando il certificato.

</dd> <dt>

*SuppliedCred* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ \_ credenziali fornita da SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) che contiene le credenziali di un ID online di cui è richiesto il certificato. Il provider di identità deve convalidare i dati di input come se provenisse da un'origine non attendibile.

</dd> <dt>

*SuppliedCredSize* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *SuppliedCred* .

</dd> <dt>

*CertContext* \[ out\]
</dt> <dd>

Se la funzione ha esito positivo, questo parametro è un puntatore al puntatore di contesto CCERT restituito \_ . Al termine dell'utilizzo del contesto del certificato, rilasciarlo chiamando la funzione [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce lo stato \_ Success.

Se la funzione ha esito negativo, la funzione può restituire uno dei codici di errore NTSTATUS seguenti.



| Valore restituito                                                                                            | Descrizione                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>STATO \_ non \_ supportato</dt> </dl>       | Il provider di identità non riconosce il tipo di credenziale delle credenziali fornite. LSA tenterà il provider di identità successivo.<br/>                                           |
| <dl> <dt>\_errore di accesso stato \_</dt> </dl>       | Le credenziali non sono corrette.<br/>                                                                                                                                                |
| <dl> <dt>STATO \_ parametro non valido \_</dt> </dl>   | Un parametro non è valido. La credenziale potrebbe essere in un formato non corretto e non nella struttura di [**\_ \_ credenziali specificata SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) .<br/> |
| <dl> <dt>rete di stato \_ \_ irraggiungibile</dt> </dl> | Il provider di identità non può contattare il cloud per ottenere il certificato.<br/>                                                                                                   |
| <dl> <dt>PASSWORD di stato \_ \_ scaduta</dt> </dl>    | La password dell'account è scaduta.<br/>                                                                                                                                           |
| <dl> <dt>\_account stato \_ bloccato \_</dt> </dl> | L'account è stato bloccato. <br/>                                                                                                                                           |
| <dl> <dt>Altro</dt> </dl>                       | Altri codici di errore specifici del provider. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Prima di recuperare il certificato dal cloud, il provider di identità deve verificare la presenza di un certificato valido per l'utente nell'archivio certificati "MY" dell'utente. Se esiste un certificato valido, il provider deve restituire questo certificato per evitare il traffico di rete superfluo.

Il provider di identità può inoltre memorizzare nella cache il certificato localmente, purché sia protetto dall'utente corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 

