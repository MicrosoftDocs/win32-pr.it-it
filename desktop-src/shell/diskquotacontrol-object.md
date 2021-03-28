---
description: Consente a un amministratore di gestire le proprietà della quota disco di un volume.
title: Oggetto DiskQuotaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 843f33ee79e70309a47f170bb1935f94f45c8f2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994901"
---
# <a name="diskquotacontrol-object"></a>Oggetto DiskQuotaControl

Consente a un amministratore di gestire le proprietà della quota disco di un volume. Il file system NTFS consente a un amministratore di gestire l'utilizzo del disco in un volume condiviso allocando a ogni utente una quantità di spazio su disco specificata o un *limite di quota*. È possibile utilizzare questo oggetto per impostare il limite di quota predefinito che verrà assegnato automaticamente a tutti i nuovi utenti.

## <a name="members"></a>Membri

L'oggetto **DiskQuotaControl** dispone di questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

L'oggetto **DiskQuotaControl** presenta questi eventi.



| Event                                                           | Descrizione                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) | Si verifica quando sono state risolte le informazioni sul nome per un oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) .<br/> |



 

### <a name="methods"></a>Metodi

L'oggetto **DiskQuotaControl** dispone di questi metodi.



| Metodo                                                                                    | Descrizione                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**AddUser**](diskquotacontrol-adduser.md)                                               | Assegna una quota disco non predefinita a un nuovo utente.<br/>                                  |
| [**DeleteUser**](diskquotacontrol-deleteuser.md)                                         | Elimina un utente dal volume.<br/>                                                 |
| [**FindUser**](diskquotacontrol-finduser.md)                                             | Trova la voce di un utente, in base al nome, nel file di quota del volume.<br/>                      |
| [**GiveUserNameResolutionPriority**](diskquotacontrol-giveusernameresolutionpriority.md) | Inserisce l'oggetto utente specificato accanto alla riga per la risoluzione dei nomi.<br/>              |
| [**Inizializzare**](diskquotacontrol-initialize.md)                                         | Apre un volume specificato e inizializza il relativo oggetto di controllo della quota.<br/>              |
| [**InvalidateSidNameCache**](diskquotacontrol-invalidatesidnamecache.md)                 | Invalida la cache del nome utente dell'ID di sicurezza.<br/>                                    |
| [**ShutdownNameResolution**](diskquotacontrol-shutdownnameresolution.md)                 | Arresta il thread di risoluzione del nome utente.<br/>                                     |
| [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md)               | Converte un nome di accesso nell'ID di sicurezza utente corrispondente in formato stringa.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **DiskQuotaControl** dispone di queste proprietà.



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta il limite di quota predefinito.<br/>                                                                                                              |
| [**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)<br/>         | Sola lettura<br/>  | Ottiene il limite di quota predefinito come stringa di testo.<br/>                                                                                                     |
| [**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta la soglia di quota predefinita.<br/>                                                                                                          |
| [**DefaultQuotaThresholdText**](diskquotacontrol-defaultquotathresholdtext.md)<br/> | Sola lettura<br/>  | Ottiene la soglia di quota predefinita come stringa di testo.<br/>                                                                                                 |
| [**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)<br/>                         | Lettura/Scrittura<br/> | Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.<br/>     |
| [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)<br/>                 | Lettura/Scrittura<br/> | Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera la soglia di quota assegnata.<br/> |
| [**QuotaFileIncomplete**](diskquotacontrol-quotafileincomplete.md)<br/>             | Sola lettura<br/>  | Ottiene un valore booleano che indica se il file di quota per il volume è completo.<br/>                                                             |
| [**QuotaFileRebuilding**](diskquotacontrol-quotafilerebuilding.md)<br/>             | Sola lettura<br/>  | Ottiene un valore booleano che indica se il file di quota per il volume è attualmente in fase di ricompilazione.<br/>                                              |
| [**QuotaState**](diskquotacontrol-quotastate.md)<br/>                               | Lettura/Scrittura<br/> | Imposta o ottiene lo stato delle quote disco del volume.<br/>                                                                                                |
| [**UserNameResolution**](diskquotacontrol-usernameresolution.md)<br/>               | Lettura/Scrittura<br/> | Imposta o ottiene un valore che controlla la modalità di risoluzione dei SID utente nei nomi utente.<br/>                                                                        |



 

## <a name="remarks"></a>Commenti

Un amministratore può utilizzare l'oggetto **DiskQuotaControl** per eseguire una serie di attività, incluse le seguenti:

-   Abilitazione e disabilitazione del sistema di quota disco del volume.
-   Ottenere lo stato del sistema di quota nel volume.
-   La negazione dello spazio su disco agli utenti supera il limite di quota.
-   Specifica della soglia di avviso e dei valori di limite di quota predefiniti che verranno assegnati ai nuovi utenti.
-   Aggiunta e rimozione di utenti.

L'oggetto **DiskQuotaControl** consente di impostare i valori predefiniti globali per il volume per le proprietà, ad esempio i limiti di quota. Tuttavia, ogni utente è rappresentato da un oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) che può essere usato per specificare le singole impostazioni di quota.

Sono disponibili diversi modi per ottenere un oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente:

-   Gli oggetti [**DIDiskQuotaUser**](didiskquotauser-object.md) per tutti gli utenti con quote nel volume vengono esposti come raccolta e possono essere enumerati. Per informazioni su come enumerare gli oggetti **DIDiskQuotaUser** , vedere **enumerazione degli utenti di quote disco** nella sezione Osservazioni di **DIDiskQuotaUser**.
-   Quando si aggiunge un nuovo utente, il metodo [**adduser**](diskquotacontrol-adduser.md) restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.
-   Se si ha il nome dell'utente, il metodo [**FindUser**](diskquotacontrol-finduser.md) restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.

Questo oggetto rende disponibili le funzionalità essenziali dell'interfaccia IDiskQuotaControl per gli script e le applicazioni basate su Microsoft Visual Basic.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Shell**](shell.md)
</dt> </dl>

 

 




