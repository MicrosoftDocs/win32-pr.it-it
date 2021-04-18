---
description: Recupera la password dell'account del servizio.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Funzione GetServiceAccountPassword (Secpkg. h)
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
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315352"
---
# <a name="getserviceaccountpassword-function"></a>GetServiceAccountPassword (funzione)

Recupera la password dell'account di servizio, disponibile per i [*provider di supporto*](/windows/desktop/SecGloss/s-gly) per la sicurezza (SSP), ad esempio SSP Kerberos.

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

*AccountName* \[ in\]
</dt> <dd>

Nome account con terminazione null dell'account del servizio gestito del gruppo (gMSA). Il nome utente può essere uno dei seguenti formati:

-   Nome dell'account SAM del gMSA.
-   Nome utente in un nome di dominio completo (FQDN), ad esempio *NomeDominio * **\\** _username_ o **www.** _dominio_* _. com \\_ * _nome_. Il nome utente deve essere solo un nome SAM. Il nome di dominio può essere un nome DNS o un nome NetBIOS.
-   Nome dell'entità utente (UPN) implicito per l'account gMSA, ad esempio *some * **@** _Domain_*_. com_*, dove, in base alla definizione di un UPN implicito, il *dominio * * *. com** è il nome DNS del dominio effettivo.

</dd> <dt>

*NomeDominio* \[ in, facoltativo\]
</dt> <dd>

Nome di dominio facoltativo con terminazione null. Questa operazione è valida solo se il parametro *AccountName* è un nome account SAM. Il nome di dominio può essere solo un nome NetBIOS o un nome di dominio completo (FQDN).

</dd> <dt>

*CredFetch* \[ in\]
</dt> <dd>

Valore dell'enumerazione [**cred \_ Fetch**](cred-fetch.md) che specifica come recuperare le credenziali.



| Valore                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <dt>**CredFetchDefault**</dt> </dl> | Il sistema operativo tenta prima di tutto di recuperare la password dalla cache locale se non è il momento di recuperare la password. Se è il momento di recuperare la password, il sistema operativo Contatta il controller di dominio; in caso contrario, restituisce le password memorizzate nella cache con un valore di stato success.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <dt>**CredFetchDPAPI**</dt> </dl>         | Restituisce le credenziali DPAPI locali al chiamante. Generalmente i provider di servizi condivisi non richiedono l'utilizzo di questo valore.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <dt>**CredFetchForced**</dt> </dl>     | Impone al sistema operativo di provare a leggere la password dal controller di dominio. Durante il tempo di rollover della password, è possibile che la password sia stata modificata nel controller di dominio e in altri host membro, ma l'host membro gMSA riconosce la password come ancora valida. Ciò può verificarsi a causa di problemi di sfasamento dell'orologio tra controller di dominio diversi. Quando si specifica questo valore, il sistema operativo determina se è possibile che si verifichi una modifica della password a causa dello sfasamento dell'orologio e, in caso affermativo, recupera la password. In caso contrario, vengono restituite le credenziali memorizzate nella cache. Se non sono presenti credenziali memorizzate nella cache, il sistema operativo tenta di ottenerne uno dal controller di dominio.<br/> |



 

</dd> <dt>

*FileTimeExpiry* \[ in, out, facoltativo\]
</dt> <dd>

In caso di input, se questo valore è diverso da null e non è un **FILETIME** zero, *FileTimeExpiry* contiene l'ora di scadenza delle credenziali dell'account del servizio note al chiamante. Se il parametro *FileTimeExpiry* è uguale a una delle credenziali correnti, la chiamata ha esito negativo. Nell'output il parametro *FileTimeExpiry* contiene l'ora di scadenza della credenziale restituita.

</dd> <dt>

*CurrentPassword* \[ out\]
</dt> <dd>

Password corrente di gMSA.

</dd> <dt>

*PreviousPassword* \[ out\]
</dt> <dd>

Password precedente di gMSA.

</dd> <dt>

*FileTimeCurrPwdValidForOutbound* \[ out, facoltativo\]
</dt> <dd>

Indica l'ora dopo la quale la password corrente è valida per le richieste in uscita. Il chiamante deve confrontare l'ora corrente con questo valore e usare la password corrente restituita solo se l'ora corrente è maggiore o uguale al valore restituito da questo parametro. L'uso di questo parametro è progettato per i chiamanti che non hanno ritentato la logica in uscita, ad esempio, NTLM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è STATUS \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice NTSTATUS. Per altre informazioni, vedere [valori restituiti della funzione di criteri LSA](management-return-values.md).

È possibile usare la funzione [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) per convertire il codice NTSTATUS in un codice di errore di Windows.

Al termine dell'uso dei buffer restituiti nei parametri *CurrentPassword* e *PreviousPassword* , è possibile liberarli chiamando la funzione [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) .

## <a name="remarks"></a>Commenti

La funzione **GetServiceAccountPassword** può essere chiamata negli scenari seguenti:

-   Dalle funzioni di accesso di Security Support Provider (SSP), il provider di servizi condivisi deve rilevare che la password dell'account del servizio \_ \_ viene utilizzata per accedere all'entità e deve verificare che il chiamante disponga del privilegio TCB o di un servizio di rete. Il provider di servizi condivisi deve consentire al processo di accesso di procedere ottenendo le credenziali più recenti chiamando la funzione **GetServiceAccountPassword** con il valore **CredFetchDefault** nell'enumerazione di [**\_ recupero cred**](cred-fetch.md) .

-   Da SSP nelle chiamate [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) e [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) . Gli SSP devono rilevare che la \_ password dell'account del servizio \_ viene usata per queste chiamate. se la chiamata è per le credenziali non primarie, il provider di servizi condivisi deve verificare che il chiamante abbia il privilegio TCB o sia un servizio di rete. Il provider di servizi condivisi deve quindi chiamare la funzione **GetServiceAccountPassword** con il valore **CredFetchDefault** nell'enumerazione [**cred \_ Fetch**](cred-fetch.md) e procedere con la chiamata. Se le chiamate a **InitializeSecurityContext** e **AcceptSecurityContext** hanno esito negativo, il provider di servizi condivisi deve usare *FileTimeExpiry* recuperato dalla chiamata precedente a **GetServiceAccountPassword** e usarlo come input per chiamare nuovamente **GetServiceAccountPassword** usando il valore **CredFetchForced** nell'enumerazione di **\_ recupero cred** . Se è disponibile una nuova credenziale gMSA, la seconda chiamata avrà esito positivo con le nuove credenziali e il provider di servizi condivisi dovrà riprovare con le nuove credenziali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 

