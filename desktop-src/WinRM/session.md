---
title: Oggetto Session (WSManDisp.h)
description: Definisce le operazioni e le impostazioni di sessione.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Oggetto sessione Windows gestione remota
- Oggetto sessione Windows gestione remota , descritto
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b63ce9aa5898f3b6dad716f7af19688059ccf7a3f48901fa73ed3250cd2660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121561"
---
# <a name="session-object-wsmandisph"></a>Oggetto Session (WSManDisp.h)

Definisce le operazioni e le impostazioni di sessione. Qualsiasi Windows di gestione remota richiede la creazione di una sessione che si connette **a** un computer remoto, a un controller di gestione [*di base*](windows-remote-management-glossary.md) (BMC) o al computer locale. Le operazioni di rete WinRM includono il recupero, la scrittura o l'enumerazione dei dati o la chiamata di metodi. I metodi **dell'oggetto Session** rispecchiano le operazioni di base definite nel WS-Management protocollo.

## <a name="members"></a>Membri

**L'oggetto Session** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Session** dispone di questi metodi.



| Metodo                                 | Descrizione                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Creare**](session-create.md)       | Crea una nuova istanza di una risorsa e restituisce l'URI del nuovo oggetto .<br/>                                      |
| [**Elimina**](session-delete.md)       | Elimina la risorsa specificata nell'URI della risorsa.<br/>                                                              |
| [**Enumerazione**](session-enumerate.md) | Enumera una raccolta, una tabella o una risorsa di log dei messaggi.<br/>                                                         |
| [**Ottieni**](session-get.md)             | Recupera una risorsa dal servizio e restituisce una rappresentazione XML dell'istanza corrente della risorsa.<br/> |
| [**Identificare**](session-identify.md)   | Esegue una query su un computer remoto per determinare se supporta il WS-Management remoto<br/>                                 |
| [**evocare**](session-invoke.md)       | Richiama un metodo che restituisce i risultati della chiamata al metodo.<br/>                                                    |
| [**Mettere**](session-put.md)             | Aggiorna una risorsa.<br/>                                                                                              |



 

### <a name="properties"></a>Proprietà

**L'oggetto Session** ha queste proprietà.



| Proprietà                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchItems**](session-batchitems.md)<br/> | Lettura/Scrittura<br/> | Imposta e ottiene il numero di elementi in ogni batch di enumerazione. Questo valore non può essere modificato durante un'enumerazione. Per impostazione predefinita, il valore predefinito è un numero illimitato di elementi. Il provider di risorse può impostare un limite.<br/> |
| [**Errore**](session-error.md)<br/>           | Sola lettura<br/>  | Ottiene informazioni aggiuntive sull'errore in un flusso XML.<br/>                                                                                                                                                              |
| [**Timeout**](session-timeout.md)<br/>       | Lettura/Scrittura<br/> | Imposta e ottiene la quantità massima di tempo (in millisecondi) di attesa dell'applicazione client.<br/>                                                                                                                   |



 

## <a name="remarks"></a>Commenti

**L'oggetto Session** corrisponde all'interfaccia [**IWSManSession.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene illustrato come creare un **oggetto** Session.


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[WinRM Scripting API](winrm-scripting-api.md)
</dt> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[Scripting in Windows Remote Management](scripting-in-windows-remote-management.md)
</dt> <dt>

[Recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





