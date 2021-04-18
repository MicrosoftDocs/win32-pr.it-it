---
description: Un campo di database del tipo di dati FormattedSDDLText contiene una stringa di testo che descrive un descrittore di sicurezza utilizzando il linguaggio SDDL (Security Descriptor Definition Language) valido. Questo tipo di dati viene utilizzato dal campo SDDLText della tabella MsiLockPermissionsEx per proteggere un oggetto selezionato. Si noti che il campo SDDLText della tabella MsiLockPermissionsEx non supporta le proprietà private o Public.
ms.assetid: a36e257d-ef3c-45db-a50e-94d7fd4e09e2
title: FormattedSDDLText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ddfeac55f05ebea5f1603def6adcbac32aa9d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309471"
---
# <a name="formattedsddltext"></a>FormattedSDDLText

Un campo di database del tipo di dati **FormattedSDDLText** contiene una stringa di testo che descrive un descrittore di sicurezza utilizzando il linguaggio SDDL ( [Security Descriptor Definition Language](../secauthz/security-descriptor-definition-language.md) ) valido. Questo tipo di dati viene utilizzato dal campo SDDLText della [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) per proteggere un oggetto selezionato. Si noti che il campo SDDLText della tabella MsiLockPermissionsEx non supporta le proprietà private o Public.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questo tipo di dati è disponibile a partire da Windows Installer 5,0.

Il tipo di dati **FormattedSDDLText** può avere una stringa SDDL scritta in un [formato di stringa descrittore di sicurezza](../secauthz/security-descriptor-string-format.md)valido. Per ulteriori informazioni su SDDL, vedere la sezione [controllo di accesso](../secauthz/access-control.md) di [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/). Inoltre, una stringa di testo **FormattedSDDLText** può utilizzare le parentesi angolari (<>) per contenere il dominio e il nome utente dell'utente il cui SID di account deve essere determinato.

Se l'utente con nome utente *UtenteEsempio* appartiene a un dominio denominato *SampleDomain*, il valore di **FormattedSDDLText** può identificare il proprietario usando la stringa SID, il nome utente e il nome di dominio o le variabili di ambiente di Windows. Ad esempio, le stringhe seguenti sono possibili.

<dl> O:*proprietario \_ della \_ stringa SID* G:Bad: (D; OICI; GA;;; BG) (A; OICI; GRGWGX;;; *\_ \_ stringa del SID del proprietario*) (A; OICI; GA;;; BA) S:ARAI (AU; SAFA; FA;;; WD  
O: <*SampleDomain \\ UTENTEESEMPIO*>G:Bad: (D; OICI; GA;;; BG) (A; OICI; GRGWGX;;; <*SampleDomain \\ UtenteEsempio*>) (A; OICI; GA;;; BA) S:ARAI (AU; SAFA; FA;;; WD  
O: <\[ % UserDomain \] \\ \[ % username \]>G:Bad: (D; OICI; GA;;; BG) (A; OICI; GRGWGX;;; <\[ % UserDomain \] \\ \[ % username \]>) (A; OICI; GA;;; BA) S:ARAI (AU; SAFA; FA;;; WD
</dl>

 

 
