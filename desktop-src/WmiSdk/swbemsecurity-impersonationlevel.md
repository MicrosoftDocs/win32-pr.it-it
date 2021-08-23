---
description: La proprietà ImpersonationLevel è un numero intero che definisce il livello di rappresentazione COM assegnato a questo oggetto.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Proprietà SWbemSecurity.ImpersonationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cde6bca09198d6e05f1ae0143ee07d1aedd465df68258303f1d6ca2b4b7699f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639581"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>Proprietà SWbemSecurity.ImpersonationLevel

La **proprietà ImpersonationLevel** è un numero intero che definisce il livello di rappresentazione COM assegnato a questo oggetto. Questa impostazione determina se i processi appartenenti Windows Management Instrumentation (WMI) possono rilevare o usare le credenziali di sicurezza quando si effettuano chiamate ad altri processi. Per altre informazioni sui livelli di rappresentazione, vedere [Impostazione della sicurezza del processo \_ \_ dell'applicazione client](setting-client-application-process-security.md).

Se non si imposta il livello di rappresentazione in modo specifico in un moniker o impostando la proprietà **SWBemSecurity.ImpersonationLevel** in un oggetto a protezione diretta, WMI imposta il livello di rappresentazione predefinito sul valore specificato nella chiave del Registro di sistema del livello di rappresentazione [predefinita](setting-the-default-process-security-level-using-vbscript.md). Se questa impostazione non è sufficiente, il provider non supporta la richiesta e la chiamata all'API WMI può non riuscire con codice di errore **wbemErrAccessDenied** (2147749891/0x80041003).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

A livello di rappresentazione DCOM, questa proprietà può essere impostata su uno dei valori seguenti:



| Valore           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anonimo**   | Nasconde le credenziali del chiamante. WMI non supporta effettivamente questo livello di rappresentazione. se uno script specifica impersonationLevel=Anonymous, WMI a upgraderà automaticamente il livello di rappresentazione a Identify. Questo è in qualche modo un esercizio inutile, tuttavia, perché è probabile che gli script che usano il livello Di identificazione non riescano.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Identificare**    | Consente agli oggetti di eseguire query sulle credenziali del chiamante. È probabile che gli script che usano questo livello di rappresentazione non riescano. Il livello di identificazione in genere non consente di controllare gli elenchi di controllo di accesso. Non sarà possibile eseguire script su computer remoti usando Identifica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | Consente agli oggetti di utilizzare le credenziali del chiamante. È consigliabile usare questo livello di rappresentazione con gli script WMI. In questo caso, lo script WMI userà le credenziali utente. di conseguenza, sarà in grado di eseguire tutte le attività che è possibile eseguire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Delegato**    | Consente agli oggetti di consentire ad altri oggetti di usare le credenziali del chiamante. La delega consente a uno script di usare le credenziali in un computer remoto e quindi di usare le credenziali in un altro computer remoto. Anche se è possibile usare questo livello di rappresentazione all'interno di script WMI, è consigliabile farlo solo se necessario perché potrebbe rappresentare un rischio per la sicurezza.<br/> Non è possibile usare il livello di rappresentazione Delegato a meno che tutti gli account utente e gli account computer coinvolti nella transazione non siano stati contrassegnati come attendibili per la delega in Active Directory. Ciò consente di ridurre al minimo i rischi per la sicurezza. Anche se un computer remoto può usare le credenziali, può farlo solo se sia il computer che qualsiasi altro computer coinvolto nella transazione sono attendibili per la delega.<br/> |



 

Come si può vedere, la rappresentazione anonima nasconde le credenziali e Identifica consente a un oggetto remoto di eseguire query sulle credenziali, ma l'oggetto remoto non può rappresentare il contesto di sicurezza. In altre parole, anche se l'oggetto remoto sa chi si è, non può "fingere" di essere l'utente. Gli script WMI che accedono ai computer remoti usando una di queste due impostazioni avranno in genere esito negativo. In realtà, anche la maggior parte degli script eseguiti nel computer locale usando una di queste due impostazioni avrà esito negativo.

Impersonate consente al servizio WMI remoto di usare il contesto di sicurezza per eseguire l'operazione richiesta. Una richiesta WMI remota che usa in genere l'impostazione Impersonate ha in genere esito positivo, purché le credenziali dispongano di privilegi sufficienti per eseguire l'operazione prevista. In altre parole, non è possibile usare WMI per eseguire un'azione (in remoto o in altro modo) che non si dispone dell'autorizzazione per eseguire all'esterno di WMI.

L'impostazione di impersonationLevel su Delegate consente al servizio WMI remoto di passare le credenziali ad altri oggetti ed è in genere considerato un rischio per la sicurezza.

È possibile impostare il livello di rappresentazione di un oggetto [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) impostando la **proprietà ImpersonationLevel** sul valore desiderato. L'esempio seguente illustra come impostare il livello di rappresentazione per un **oggetto SWbemObject:**


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



È anche possibile specificare i livelli di rappresentazione come parte di un moniker. L'esempio seguente imposta il livello di autenticazione e il livello di rappresentazione e recupera un'istanza del [**servizio Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service).


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Impostazione della sicurezza \_ del processo \_ dell'applicazione client](setting-client-application-process-security.md)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

