---
description: Rimuove un computer da un dominio o un gruppo di lavoro.
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
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878245"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Metodo UnjoinDomainOrWorkgroup della \_ classe ComputerSystem Win32

Il metodo **UnjoinDomainOrWorkgroup** rimuove un computer da un dominio o un gruppo di lavoro.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*Password* \[ di in\]
</dt> <dd>

Se il parametro *username* specifica un nome di account, il parametro *password* deve puntare alla password da usare per la connessione al controller di dominio. In caso contrario, questo parametro deve essere **null**.

> [!Note]  
> Per la connessione a winmgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sul puntatore [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) , la *password* deve usare un livello di autenticazione elevato, non inferiore alla **\_ \_ \_ \_ \_ privacy PKT del livello auth C**. Se da locale a winmgmt, questo non rappresenta un problema.

 

</dd> <dt>

*Nome utente* \[ in\]
</dt> <dd>

Puntatore a una stringa di caratteri con terminazione null costante che specifica il nome dell'account da utilizzare per la connessione al controller di dominio. È necessario specificare un dominio e un account utente, ad esempio "dominio \\ utente" o " user@domain ". Se questo parametro è **null**, viene utilizzato il contesto del chiamante.

> [!Note]  
> Il *nome utente* deve usare un livello di autenticazione elevato, non inferiore alla **\_ \_ \_ \_ \_ privacy PKT del livello auth C**, quando si connette a winmgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sul puntatore [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . Se da locale a winmgmt, questo non rappresenta un problema.

 

</dd> <dt>

*FUnjoinOptions* \[ in\]
</dt> <dd>

Set di flag di bit che definiscono le opzioni di Unjoin.

<dt>



  (0)


</dt> <dd>

Valore predefinito. Nessuna opzione.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**Netsetup \_ \_Eliminazione Acct** (4)


</dt> <dd>

Disabilitare l'account Active Directory dopo l'operazione di Unjoin, ma non eliminare l'account.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo **UnjoinDomainOrWorkgroup** restituisce 0 (zero) in caso di esito positivo o se non è presente alcuna opzione. Qualsiasi altro valore indica un errore. Per i codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Altro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Dopo aver chiamato questo metodo, riavviare il computer interessato per applicare le modifiche.

## <a name="examples"></a>Esempio

[Separare un computer da un dominio](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) L'esempio VBScript consente di separare il computer locale dal dominio corrente e di disabilitare l'account del computer.

L'esempio di [Unjoin a computer da un dominio che utilizza lo script vbs](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) è un join di un computer specificato da un dominio. .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ComputerSystem Win32**](win32-computersystem.md)
</dt> <dt>

[**Metodo JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

