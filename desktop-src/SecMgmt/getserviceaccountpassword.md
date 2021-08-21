---
description: Recupera la password dell'account del servizio.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Funzione GetServiceAccountPassword (Secpkg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: dc00dc01d3acd996257ebc4056be573335a1fd209e9d38abbdcb6bab33124b4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894774"
---
# <a name="getserviceaccountpassword-function"></a>Funzione GetServiceAccountPassword

Recupera la password dell'account del servizio, disponibile [*per i provider*](/windows/desktop/SecGloss/s-gly) di supporto della sicurezza (SSP), ad esempio Kerberos SSP.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AccountName* \[ Pollici\]
</dt> <dd>

Nome dell'account del servizio gestito del gruppo con terminazione Null. Il nome utente può essere uno dei formati seguenti:

-   Nome dell'account SAM dell'account del servizio gestione account del gruppo.
-   Nome utente in un nome di dominio completo (FQDN), ad esempio *DomainName* **\\** _UserName_ o **www.** _dominio_* _.com \\_ * _nome_. Il nome utente deve essere solo un nome SAM. Il nome di dominio può essere un nome DNS o un nome NetBIOS.
-   Nome dell'entità utente (UPN) implicito per l'account gMSA, ad esempio *SomeName* **@** _Domain_*_.com_* dove, in base alla definizione di un UPN implicito, *Domain**.com** è il nome DNS del dominio effettivo.

</dd> <dt>

*NomeDominio* \[ in, facoltativo\]
</dt> <dd>

Nome di dominio con terminazione Null facoltativo. Questo valore è valido solo se il *parametro AccountName* è un nome di account SAM. Il nome di dominio può essere solo un nome NetBIOS o un nome di dominio completo (FQDN).

</dd> <dt>

*CredFetch* \[ Pollici\]
</dt> <dd>

Valore [**dell'enumerazione CRED \_ FETCH**](cred-fetch.md) che specifica come recuperare le credenziali.



| Valore                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <dt>**CredFetchDefault**</dt> </dl> | Il sistema operativo tenta prima di tutto di recuperare la password dalla cache locale se non è il momento di recuperarla. Se è il momento di recuperare la password, il sistema operativo contatta il controller di dominio, in caso contrario, restituisce le password memorizzate nella cache con un valore di stato positivo.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <dt>**CredFetchDPAPI**</dt> </dl>         | Restituisce le credenziali DPAPI locali al chiamante. Gli SSP in genere non richiedono l'uso di questo valore.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <dt>**CredFetchForced**</dt> </dl>     | Forza il sistema operativo a tentare di leggere la password dal controller di dominio. Durante il tempo di rollover della password, la password potrebbe essere stata modificata nel controller di dominio e in altri host membro, ma l'host membro del gruppo di gestione delle password riconosce la password come ancora valida. Ciò può verificarsi a causa di problemi di avallo dell'orologio tra controller di dominio diversi. Quando si specifica questo valore, il sistema operativo determina se è possibile modificare la password a causa di un'avallata dell'orologio e, in tal caso, recupera la password. In caso contrario, viene restituita la credenziale memorizzata nella cache. Se non sono presenti credenziali memorizzate nella cache, il sistema operativo tenta di ottenerne una dal controller di dominio.<br/> |



 

</dd> <dt>

*FileTimeExpiry* \[ in, out, facoltativo\]
</dt> <dd>

In input, se questo valore è diverso da null e non è un **valore FILETIME** pari a zero, *FileTimeExpiry* contiene l'ora di scadenza delle credenziali dell'account del servizio come noto al chiamante. Se il *parametro FileTimeExpiry* corrisponde a una delle credenziali correnti, la chiamata ha esito negativo. Nell'output, *il parametro FileTimeExpiry* contiene l'ora di scadenza della credenziale restituita.

</dd> <dt>

*CurrentPassword* \[ Cambio\]
</dt> <dd>

Password corrente dell'amministratore del sistema gMSA.

</dd> <dt>

*PreviousPassword* \[ Cambio\]
</dt> <dd>

Password precedente dell'amministratore del sistema gMSA.

</dd> <dt>

*FileTimeCurrPwdValidForOutbound* \[ out, facoltativo\]
</dt> <dd>

Indica l'ora dopo la quale la password corrente è valida per le richieste in uscita. Il chiamante deve confrontare l'ora corrente con questo valore e usare la password corrente restituita solo se l'ora corrente è maggiore o uguale al valore restituito da questo parametro. L'uso di questo parametro è progettato per i chiamanti che non hanno tentativi nella logica in uscita, ad esempio NTLM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è STATUS \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice NTSTATUS. Per altre informazioni, vedere [Valori restituiti della funzione criteri LSA](management-return-values.md).

È possibile usare la [**funzione LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) per convertire il codice NTSTATUS in un Windows di errore.

Al termine dell'uso dei buffer restituiti nei *parametri CurrentPassword* e *PreviousPassword,* liberarli chiamando la [**funzione FreeLsaHeap.**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap)

## <a name="remarks"></a>Commenti

La **funzione GetServiceAccountPassword** può essere chiamata negli scenari seguenti:

-   Dalle funzioni di accesso dei provider di supporto per la sicurezza (SSP), il provider di servizi condivisi deve rilevare che la PASSWORD DELL'ACCOUNT DEL SERVIZIO viene usata per accedere all'entità e deve verificare che il chiamante abbia il privilegio TCB o sia un servizio di \_ \_ rete. Il provider di servizi condivisi deve quindi consentire al processo di accesso di procedere ottenendo le credenziali più recenti chiamando la funzione **GetServiceAccountPassword** con il valore **CredFetchDefault** nell'enumerazione [**CRED \_ FETCH.**](cred-fetch.md)

-   Dagli SSP nelle chiamate [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) [**e AcceptSecurityContext.**](../SecAuthN/acceptsecuritycontext--general.md) I provider di servizi condivisi devono rilevare che la PASSWORD DELL'ACCOUNT DEL SERVIZIO viene usata per queste chiamate e, se la chiamata è per credenziali non privilegiate, il provider di servizi condivisi deve assicurarsi che il chiamante abbia il privilegio TCB o sia un servizio di \_ \_ rete. Il provider di servizi condivisi deve quindi chiamare la **funzione GetServiceAccountPassword** con il **valore CredFetchDefault** nell'enumerazione [**CRED \_ FETCH**](cred-fetch.md) e procedere con la chiamata. Se le chiamate **InitializeSecurityContext** e **AcceptSecurityContext** hanno esito negativo, il provider di servizi condivisi deve usare il valore *FileTimeExpiry* recuperato dalla chiamata precedente a **GetServiceAccountPassword** e usarlo come input per chiamare di nuovo **GetServiceAccountPassword** usando il valore **CredFetchForced** nell'enumerazione **CRED \_ FETCH.** Se è disponibile una nuova credenziale gMSA, la seconda chiamata avrà esito positivo con nuove credenziali e il provider di servizi condivisi dovrà quindi riprovare con le nuove credenziali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Secpkg.h</dt> </dl> |



 

