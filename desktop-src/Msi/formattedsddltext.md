---
description: Un campo di database con tipo di dati FormattedSDDLText contiene una stringa di testo che descrive un descrittore di sicurezza usando un linguaggio SDDL (Security Descriptor Definition Language) valido. Questo tipo di dati viene usato dal campo SDDLText della tabella MsiLockPermissionsEx per proteggere un oggetto selezionato. Si noti che il campo SDDLText della tabella MsiLockPermissionsEx non supporta le proprietà private o pubbliche.
ms.assetid: a36e257d-ef3c-45db-a50e-94d7fd4e09e2
title: FormattedSDDLText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdfc4446c4362646e8c275ec427f759b8aec6a257d5221926431434688b91c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142890"
---
# <a name="formattedsddltext"></a>FormattedSDDLText

Un campo di database con tipo di dati **FormattedSDDLText** contiene una stringa di testo che descrive un descrittore di sicurezza usando un linguaggio SDDL [(Security Descriptor Definition Language)](../secauthz/security-descriptor-definition-language.md) valido. Questo tipo di dati viene usato dal campo SDDLText della tabella [MsiLockPermissionsEx per](msilockpermissionsex-table.md) proteggere un oggetto selezionato. Si noti che il campo SDDLText della tabella MsiLockPermissionsEx non supporta le proprietà private o pubbliche.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questo tipo di dati è disponibile a partire da Windows Installer 5.0.

Il **tipo di dati FormattedSDDLText** può contenere una stringa SDDL scritta in formato stringa [descrittore di sicurezza valido.](../secauthz/security-descriptor-string-format.md) Per altre informazioni su SDDL, vedere la sezione [Controllo](../secauthz/access-control.md) di accesso di [Microsoft Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) Inoltre, una stringa di testo **FormattedSDDLText** può usare parentesi angolari (<>) per contenere il dominio e il nome utente dell'utente di cui determinare il SID dell'account.

Se l'utente con nome utente *SampleUser* appartiene a un dominio denominato *SampleDomain,* il **valore FormattedSDDLText** può identificare il proprietario usando la stringa SID, il nome utente e il nome di dominio o le variabili di ambiente Windows. Ad esempio, le stringhe seguenti sono possibili.

<dl> O:*owner \_ sid \_ string* G:BAD:(D;OICI;GA;;; BG)(A;OICI;GRGWGX;;; *owner \_ sid \_ string*)(A;OICI;GA;;; BA)S:ARAI(AU; SAFA;FA;;; WD)  
O:<*SampleDomain \\ SampleUser*>G:BAD:(D;OICI;GA;;; BG)(A;OICI;GRGWGX;;; <*SampleDomain \\ SampleUser*>)(A;OICI;GA;;; BA)S:ARAI(AU; SAFA;FA;;; WD)  
O:<\[ %USERDOMAIN \] \\ \[ %USERNAME \]>G:BAD:(D;OICI;GA;;; BG)(A;OICI;GRGWGX;;; <\[ %USERDOMAIN \] \\ \[ %USERNAME \]>)(A;OICI;GA;;; BA)S:ARAI(AU; SAFA;FA;;; WD)
</dl>

 

 
