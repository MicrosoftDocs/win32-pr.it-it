---
description: Rimuove un sistema di computer da un dominio o un gruppo di lavoro.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Metodo UnjoinDomainOrWorkgroup della classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 992aa6c84f912f705e02252d1ac6d24422934edb991c049de188ab5fb0ccbfa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105071"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Metodo UnjoinDomainOrWorkgroup della classe ComputerSystem Win32 \_

Il **metodo UnjoinDomainOrWorkgroup** rimuove un sistema di computer da un dominio o un gruppo di lavoro.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Password* \[ Pollici\]
</dt> <dd>

Se il *parametro UserName* specifica un nome di account, il *parametro Password* deve puntare alla password da usare per la connessione al controller di dominio. In caso contrario, questo parametro deve essere **NULL.**

> [!Note]  
> *Per* la connessione a Winmgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) nel puntatore [**IWbemServices,**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) la password deve usare un livello di autenticazione elevato, non inferiore a **RPC \_ \_ CAUTHN \_ LEVEL \_ PKT \_ PRIVACY.** Se locale a Winmgmt, questo non è un problema.

 

</dd> <dt>

*UserName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa di caratteri con terminazione Null costante che specifica il nome dell'account da utilizzare per la connessione al controller di dominio. Deve specificare un dominio e un account utente, ad esempio "utente \\ di dominio" o " user@domain ". Se questo parametro è **NULL,** viene usato il contesto del chiamante.

> [!Note]  
> *UserName* deve usare un livello di autenticazione elevato, non inferiore a **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY,** quando ci si connette a Winmgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sul puntatore [**IWbemServices.**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) Se locale a Winmgmt, questo non è un problema.

 

</dd> <dt>

*FUnjoinOptions* \[ Pollici\]
</dt> <dd>

Set di flag di bit che definiscono le opzioni non contigue.

<dt>



  (0)


</dt> <dd>

Valore predefinito. Nessuna opzione.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP \_ ACCT \_ DELETE** (4)


</dt> <dd>

Disabilitare l'account Active Directory dopo l'operazione di annullamento dell'unione, ma non eliminare l'account.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Il **metodo UnjoinDomainOrWorkgroup** restituisce 0 (zero) in caso di esito positivo o quando non sono coinvolte opzioni. Qualsiasi altro valore indica un errore. Per i codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Altro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Dopo aver chiamato questo metodo, riavviare il computer interessato per applicare le modifiche.

## <a name="examples"></a>Esempio

[Scollegare un computer da un dominio](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) L'esempio VBScript scollega il computer locale dal dominio corrente e disabilita l'account computer.

[L'esempio Disinserisce](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) un computer da un dominio usando lo script VBS annulla l'accesso a un computer specificato da un dominio. .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ ComputerSystem**](win32-computersystem.md)
</dt> <dt>

[**Metodo JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

