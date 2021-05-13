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
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841552"
---
# <a name="diskquotacontrol-object"></a>Oggetto DiskQuotaControl

Consente a un amministratore di gestire le proprietà della quota disco di un volume. L'file system NTFS consente a un amministratore di gestire l'utilizzo del disco in un volume condiviso allocando una quantità specificata di spazio su disco, o limite di *quota,* a ogni utente. È possibile usare questo oggetto per impostare il limite di quota predefinito che verrà assegnato automaticamente a tutti i nuovi utenti.

## <a name="members"></a>Membri

**L'oggetto DiskQuotaControl** ha questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

**L'oggetto DiskQuotaControl** include questi eventi.



| Event                                                           | Descrizione                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) | Si verifica quando le informazioni sul nome per [**un oggetto DIDiskQuotaUser**](didiskquotauser-object.md) sono state risolte.<br/> |



 

### <a name="methods"></a>Metodi

**L'oggetto DiskQuotaControl** dispone di questi metodi.



| Metodo                                                                                    | Descrizione                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**AddUser**](diskquotacontrol-adduser.md)                                               | Assegna una quota disco non predefinita a un nuovo utente.<br/>                                  |
| [**DeleteUser**](diskquotacontrol-deleteuser.md)                                         | Elimina un utente dal volume.<br/>                                                 |
| [**FindUser**](diskquotacontrol-finduser.md)                                             | Trova la voce di un utente, in base al nome, nel file di quota del volume.<br/>                      |
| [**GiveUserNameResolutionPriority**](diskquotacontrol-giveusernameresolutionpriority.md) | Posiziona l'oggetto utente specificato nella riga successiva per la risoluzione dei nomi.<br/>              |
| [**Inizializzare**](diskquotacontrol-initialize.md)                                         | Apre un volume specificato e inizializza il relativo oggetto di controllo della quota.<br/>              |
| [**InvalidateSidNameCache**](diskquotacontrol-invalidatesidnamecache.md)                 | Invalida la cache dei nomi utente dell'ID di sicurezza.<br/>                                    |
| [**ShutdownNameResolution**](diskquotacontrol-shutdownnameresolution.md)                 | Arresta il thread di risoluzione dei nomi utente.<br/>                                     |
| [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md)               | Converte un nome di accesso nell'ID di sicurezza utente corrispondente in formato stringa.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto DiskQuotaControl** ha queste proprietà.



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)<br/>                 | Lettura/Scrittura<br/> | Imposta o ottiene il limite di quota predefinito.<br/>                                                                                                              |
| [**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)<br/>         | Sola lettura<br/>  | Ottiene il limite di quota predefinito come stringa di testo.<br/>                                                                                                     |
| [**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)<br/>         | Lettura/Scrittura<br/> | Imposta o ottiene la soglia di quota predefinita.<br/>                                                                                                          |
| [**DefaultQuotaThresholdText**](diskquotacontrol-defaultquotathresholdtext.md)<br/> | Sola lettura<br/>  | Ottiene la soglia di quota predefinita come stringa di testo.<br/>                                                                                                 |
| [**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)<br/>                         | Lettura/Scrittura<br/> | Imposta o ottiene un valore booleano che indica se verrà effettuata una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.<br/>     |
| [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)<br/>                 | Lettura/Scrittura<br/> | Imposta o ottiene un valore booleano che indica se verrà effettuata una voce del registro eventi di sistema quando un utente supera la soglia di quota assegnata.<br/> |
| [**QuotaFileIncomplete**](diskquotacontrol-quotafileincomplete.md)<br/>             | Sola lettura<br/>  | Ottiene un valore booleano che indica se il file di quota per il volume è completo.<br/>                                                             |
| [**QuotaFileRebuilding**](diskquotacontrol-quotafilerebuilding.md)<br/>             | Sola lettura<br/>  | Ottiene un valore booleano che indica se è in corso la ricompila del file di quota per il volume.<br/>                                              |
| [**QuotaState**](diskquotacontrol-quotastate.md)<br/>                               | Lettura/Scrittura<br/> | Imposta o ottiene lo stato delle quote disco del volume.<br/>                                                                                                |
| [**UserNameResolution**](diskquotacontrol-usernameresolution.md)<br/>               | Lettura/Scrittura<br/> | Imposta o ottiene un valore che controlla la modalità di risoluzione del SID dell'utente nei nomi utente.<br/>                                                                        |



 

## <a name="remarks"></a>Commenti

Un amministratore può usare **l'oggetto DiskQuotaControl** per eseguire una serie di attività, tra cui:

-   Abilitazione e disabilitazione del sistema di quota disco del volume.
-   Recupero dello stato del sistema di quote nel volume.
-   Negazione dello spazio su disco agli utenti che superano il limite di quota.
-   Specifica dei valori predefiniti di soglia di avviso e limite di quota che verranno assegnati ai nuovi utenti.
-   Aggiunta e rimozione di utenti.

**L'oggetto DiskQuotaControl** consente di impostare i valori predefiniti globali per il volume per proprietà quali i limiti di quota. Tuttavia, ogni utente è rappresentato da un [**oggetto DIDiskQuotaUser**](didiskquotauser-object.md) che può essere usato per specificare singole impostazioni di quota.

Esistono diversi modi per ottenere l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) di un utente:

-   Gli [**oggetti DIDiskQuotaUser**](didiskquotauser-object.md) per tutti gli utenti con quote nel volume vengono esposti come raccolta e possono essere enumerati. Per informazioni su come enumerare **gli oggetti DIDiskQuotaUser,** vedere Enumerazione degli utenti della **quota** del disco nella sezione Osservazioni di **DIDiskQuotaUser.**
-   Quando si aggiunge un nuovo utente, il [**metodo AddUser**](diskquotacontrol-adduser.md) restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.
-   Se si ha il nome dell'utente, il [**metodo FindUser**](diskquotacontrol-finduser.md) restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.

Questo oggetto rende disponibili le funzionalità essenziali dell'interfaccia IDiskQuotaControl per gli script e le applicazioni basate Visual Basic Microsoft.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto shell**](shell.md)
</dt> </dl>

 

 




