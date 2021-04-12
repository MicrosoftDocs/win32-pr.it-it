---
description: La proprietà AuthenticationLevel è un numero intero che definisce il livello di autenticazione COM assegnato a questo oggetto.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: Proprietà SWbemSecurity. AuthenticationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344711"
---
# <a name="swbemsecurityauthenticationlevel-property"></a>Proprietà SWbemSecurity. AuthenticationLevel

La proprietà **AuthenticationLevel** è un numero intero che definisce il livello di autenticazione com assegnato a questo oggetto. Questa impostazione determina la modalità di protezione delle informazioni inviate da WMI. Per ulteriori informazioni sui livelli di autenticazione, vedere [impostazione della \_ sicurezza del \_ processo dell'applicazione client](setting-client-application-process-security.md). In generale, non è necessario impostare il livello di autenticazione quando si effettuano chiamate API WMI. Se non si imposta questa proprietà, verrà utilizzato il livello di autenticazione COM predefinito per il sistema.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

L'impostazione authenticationLevel consente di richiedere il livello di autenticazione e privacy DCOM da usare in una connessione. Le impostazioni variano da nessuna autenticazione all'autenticazione crittografata per pacchetto.



| Valore        | Descrizione                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nessuno         | Non usa alcuna autenticazione. Tutte le impostazioni di sicurezza vengono ignorate.<br/>                                                                                                                                                                                                                                         |
| Predefinito      | Usa una negoziazione di sicurezza standard per selezionare un livello di autenticazione. Si tratta dell'impostazione consigliata, perché il client associato alla transazione verrà negoziato al livello di autenticazione specificato dal server.<br/> DCOM non seleziona il valore None durante una sessione di negoziazione.<br/> |
| Connessione      | Autentica le credenziali del client solo quando il client tenta di connettersi al server. Dopo la connessione, non viene eseguito alcun controllo di autenticazione aggiuntivo.<br/>                                                                                                                          |
| Chiamata         | Autentica le credenziali del client solo all'inizio di ogni chiamata, quando il server riceve la richiesta. Le intestazioni dei pacchetti sono firmate, ma i pacchetti di dati scambiati tra il client e il server non sono firmati né crittografati.<br/>                                                     |
| PKT          | Autentica che tutti i pacchetti di dati vengono ricevuti dal client previsto. Simile a Call; le intestazioni di pacchetto sono firmate ma non crittografate. I pacchetti stessi non sono né firmati né crittografati.<br/>                                                                                                               |
| PktIntegrity | Autentica e verifica che nessuno dei pacchetti di dati trasferiti tra il client e il server sia stato modificato. Ogni pacchetto di dati è firmato, assicurando che i pacchetti non siano stati modificati durante il transito. Nessuno dei pacchetti di dati è crittografato.<br/>                                            |
| Su PktPrivacy   | Autentica tutti i livelli di rappresentazione precedenti e firma e crittografa ogni pacchetto di dati. In questo modo si garantisce che tutte le comunicazioni tra il client e il server siano riservate.<br/>                                                                                                                             |



 

È possibile impostare il livello di autenticazione degli oggetti [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) impostando la proprietà **AuthenticationLevel** sul valore desiderato.

Nell'esempio seguente viene illustrato come impostare il livello di autenticazione per un oggetto **SwbemObject** .


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



È anche possibile specificare i livelli di autenticazione come parte di un moniker. Nell'esempio seguente viene impostato il livello di autenticazione e il livello di rappresentazione e viene recuperata un'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSECURITY CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMSECURITY IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Impostazione della \_ sicurezza del processo dell'applicazione client \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> </dl>

 

