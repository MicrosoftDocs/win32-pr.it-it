---
description: La proprietà AuthenticationLevel è un numero intero che definisce il livello di autenticazione COM assegnato a questo oggetto.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: SWbemSecurity.AuthenticationLevel - proprietà
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
ms.openlocfilehash: 0cbb765241fabb86a14a5d74f7a839d5d81b017856b6da349b9ec04fd8535a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312715"
---
# <a name="swbemsecurityauthenticationlevel-property"></a>SWbemSecurity.AuthenticationLevel - proprietà

La **proprietà AuthenticationLevel** è un numero intero che definisce il livello di autenticazione COM assegnato a questo oggetto. Questa impostazione determina la modalità di protezione delle informazioni inviate da WMI. Per altre informazioni sui livelli di autenticazione, vedere [Impostazione della sicurezza del processo \_ \_ dell'applicazione client.](setting-client-application-process-security.md) In generale, non è necessario impostare il livello di autenticazione quando si effettuano chiamate API WMI. Se non si imposta questa proprietà, viene usato il livello di autenticazione COM predefinito per il sistema.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

L'impostazione authenticationLevel consente di richiedere il livello di autenticazione DCOM e la privacy da usare in tutta una connessione. Impostazioni da nessuna autenticazione all'autenticazione crittografata per pacchetto.



| Valore        | Descrizione                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nessuno         | Non usa alcuna autenticazione. Tutte le impostazioni di sicurezza vengono ignorate.<br/>                                                                                                                                                                                                                                         |
| Predefinito      | Usa una negoziazione di sicurezza standard per selezionare un livello di autenticazione. Questa è l'impostazione consigliata perché il client coinvolto nella transazione verrà negoziato con il livello di autenticazione specificato dal server.<br/> DCOM non selezionerà il valore None durante una sessione di negoziazione.<br/> |
| Connettere      | Autentica le credenziali del client solo quando il client tenta di connettersi al server. Dopo che è stata stabilita una connessione, non vengono eseguiti controlli di autenticazione aggiuntivi.<br/>                                                                                                                          |
| Chiamata         | Autentica le credenziali del client solo all'inizio di ogni chiamata, quando il server riceve la richiesta. Le intestazioni dei pacchetti sono firmate, ma i pacchetti di dati s scambiati tra il client e il server non sono firmati né crittografati.<br/>                                                     |
| Pkt          | Autentica che tutti i pacchetti di dati vengono ricevuti dal client previsto. Simile a Call; Le intestazioni dei pacchetti sono firmate ma non crittografate. I pacchetti stessi non sono firmati né crittografati.<br/>                                                                                                               |
| PktIntegrity | Autentica e verifica che nessuno dei pacchetti di dati trasferiti tra il client e il server sia stato modificato. Ogni pacchetto di dati viene firmato, assicurandosi che i pacchetti non siano stati modificati durante il transito. Nessuno dei pacchetti di dati è crittografato.<br/>                                            |
| PktPrivacy   | Autentica tutti i livelli di rappresentazione precedenti e firma e crittografa ogni pacchetto di dati. Ciò garantisce che tutte le comunicazioni tra il client e il server siano riservate.<br/>                                                                                                                             |



 

È possibile impostare il livello di autenticazione degli oggetti [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) impostando la **proprietà AuthenticationLevel** sul valore desiderato.

L'esempio seguente illustra come impostare il livello di autenticazione per **un oggetto SwbemObject.**


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



È anche possibile specificare i livelli di autenticazione come parte di un moniker. Nell'esempio seguente vengono impostate il livello di autenticazione e il livello di rappresentazione e viene recuperata un'istanza di [**\_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
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

[Impostazione della sicurezza \_ del processo \_ dell'applicazione client](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> </dl>

 

