---
description: La tabella MsiLockPermissionsEx può essere utilizzata per proteggere servizi, file, chiavi del registro di sistema e cartelle create.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Tabella MsiLockPermissionsEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317124"
---
# <a name="msilockpermissionsex-table"></a>Tabella MsiLockPermissionsEx

La tabella MsiLockPermissionsEx può essere utilizzata per proteggere servizi, file, chiavi del registro di sistema e cartelle create.

Un pacchetto non deve contenere sia la tabella MsiLockPermissionsEx che la [tabella LockPermissions](lockpermissions-table.md).

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questa tabella è consigliata per i pacchetti destinati all'installazione con Windows Installer 5,0 o versione successiva.

La tabella MsiLockPermissionsEx include le colonne seguenti.



| Colonna               | Tipo                                       | Chiave | Nullable |
|----------------------|--------------------------------------------|-----|----------|
| MsiLockPermissionsEx | [Text](text.md)                           | S   | N        |
| LockObject           | [Identificatore](identifier.md)               | N   | N        |
| Tabella                | [Text](text.md)                           | N   | N        |
| SDDLText             | [FormattedSDDLText](formattedsddltext.md) | N   | N        |
| Condizione            | [Condition](condition.md)                 | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx
</dt> <dd>

Si tratta della chiave primaria della tabella.

</dd> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Questa colonna e la colonna della tabella consentono di specificare il file, la directory, la chiave del registro di sistema o il servizio che deve essere protetto. La colonna LockObject è una chiave esterna che punta alla chiave primaria della tabella specificata dalla colonna della tabella.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Questa colonna e la colonna LockObject specificano il file, la directory, la chiave del registro di sistema o il servizio che deve essere protetto. Nella colonna della tabella immettere file, Registry, CreateFolder o ServiceInstall per specificare un LockObject elencato nella tabella [file](file-table.md), tabella Registro di [sistema](registry-table.md), tabella [CreateFolder](createfolder-table.md)o [tabella ServiceInstall](serviceinstall-table.md).

</dd> <dt>

<span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText
</dt> <dd>

Immettere la stringa SDDL per indicare le autorizzazioni da applicare all'oggetto selezionato. L'SDDL deve essere specificato nel [formato stringa del descrittore di sicurezza](../secauthz/security-descriptor-string-format.md).

Questo non supporta le proprietà private o Public.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Questa colonna contiene un'espressione condizionale utilizzata per determinare se applicare l'autorizzazione specificata. Se la condizione restituisce **false**, l'autorizzazione non viene applicata. Se la condizione restituisce **true**, viene applicata l'autorizzazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sulla protezione di servizi, file, chiavi del registro di sistema e cartelle create, vedere la pagina relativa alla [protezione delle risorse](securing-resources-.md).

Usare la tabella MsiLockPermissionsEx per proteggere gli oggetti per un account utente che viene creato durante l'installazione. L'account utente deve esistere già quando l'installazione protegge l'oggetto. Creare l'account utente prima di installare il file, la chiave del registro di sistema, la cartella o il servizio protetto.

Se una LockObject e una coppia di tabelle in questa tabella hanno più di un'espressione condizionale che restituisce true, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1942.

Se la stringa [FormattedSDDLText](formattedsddltext.md) nel campo SDDLText non può essere risolta in una stringa SDDL valida, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1943.

Se l'utente non dispone di privilegi sufficienti per impostare il descrittore di sicurezza specificato dal campo SDDLText in un file o una cartella, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1926.

Se l'utente non dispone di privilegi sufficienti per impostare il descrittore di sicurezza specificato dal campo SDDLText in una chiave del registro di sistema, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1401.

Se l'utente non dispone di privilegi sufficienti per impostare il descrittore di sicurezza specificato dal campo SDDLText in un servizio, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1944.

## <a name="validation"></a>Convalida

<dl>

[ICE104](ice-104.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 
