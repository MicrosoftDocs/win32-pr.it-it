---
description: La tabella MsiLockPermissionsEx può essere usata per proteggere servizi, file, chiavi del Registro di sistema e cartelle create.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Tabella MsiLockPermissionsEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bff3d97bc6cd6003470b1be7d1feb20b385701d332ba852a660aa4ff6c57271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119294801"
---
# <a name="msilockpermissionsex-table"></a>Tabella MsiLockPermissionsEx

La tabella MsiLockPermissionsEx può essere usata per proteggere servizi, file, chiavi del Registro di sistema e cartelle create.

Un pacchetto non deve contenere sia la tabella MsiLockPermissionsEx che la [tabella LockPermissions](lockpermissions-table.md).

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questa tabella è consigliata per i pacchetti destinati all'installazione con Windows Installer 5.0 o versione successiva.

La tabella MsiLockPermissionsEx include le colonne seguenti.



| Colonna               | Tipo                                       | Chiave | Nullable |
|----------------------|--------------------------------------------|-----|----------|
| MsiLockPermissionsEx | [Text](text.md)                           | S   | N        |
| LockObject           | [Identificatore](identifier.md)               | N   | N        |
| Tabella                | [Text](text.md)                           | N   | N        |
| SDDLText             | [FormattedSDDLText](formattedsddltext.md) | N   | N        |
| Condition            | [Condition](condition.md)                 | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx
</dt> <dd>

Si tratta della chiave primaria di questa tabella.

</dd> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Questa colonna e la colonna Tabella specificano insieme il file, la directory, la chiave del Registro di sistema o il servizio che deve essere protetto. La colonna LockObject è una chiave esterna che punta alla chiave primaria della tabella specificata dalla colonna Table.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Questa colonna e la colonna LockObject specificano il file, la directory, la chiave del Registro di sistema o il servizio che deve essere protetto. Nella colonna Tabella immettere File, Registro di sistema, CreateFolder o ServiceInstall per specificare un LockObject elencato nella tabella [file](file-table.md) [,](registry-table.md)nella tabella del Registro di sistema, nella [tabella CreateFolder](createfolder-table.md)o nella tabella [ServiceInstall](serviceinstall-table.md).

</dd> <dt>

<span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText
</dt> <dd>

Immettere la stringa SDDL per indicare le autorizzazioni da applicare all'oggetto selezionato. Il file SDDL deve essere specificato nel formato [di stringa del descrittore di sicurezza](../secauthz/security-descriptor-string-format.md).

Non supporta le proprietà private o pubbliche.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Questa colonna contiene un'espressione condizionale utilizzata per determinare se applicare l'autorizzazione specificata. Se la condizione restituisce **FALSE,** l'autorizzazione non viene applicata. Se la condizione restituisce **TRUE, viene** applicata l'autorizzazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per [altre informazioni sulla protezione di](securing-resources-.md)servizi, file, chiavi del Registro di sistema e cartelle create, vedere Protezione delle risorse.

Usare la tabella MsiLockPermissionsEx per proteggere gli oggetti per un account utente creato durante l'installazione. L'account utente deve esistere già quando l'installazione protegge l'oggetto. Creare l'account utente prima di installare il file, la chiave del Registro di sistema, la cartella o il servizio protetto.

Se una coppia LockObject e Table in questa tabella contiene più di un'espressione condizionale che restituisce true, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1942.

Se la stringa [FormattedSDDLText](formattedsddltext.md) nel campo SDDLText non può essere risolta in una stringa SDDL valida, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1943.

Se l'utente non dispone di privilegi sufficienti per impostare il descrittore di sicurezza specificato dal campo SDDLText in un file o in una cartella, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1926.

Se l'utente non dispone di privilegi sufficienti per impostare il descrittore di sicurezza specificato dal campo SDDLText in una chiave del Registro di sistema, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1401.

Se l'utente non dispone di privilegi sufficienti per impostare il descrittore di sicurezza specificato dal campo SDDLText in un servizio, l'installazione non riesce e Windows Installer restituisce un messaggio di errore 1944.

## <a name="validation"></a>Convalida

<dl>

[ICE104](ice-104.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 
