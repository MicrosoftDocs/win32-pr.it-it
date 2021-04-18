---
description: WMI dispone di diversi oggetti helper di scripting che forniscono le conversioni richieste dagli script.
ms.assetid: 832660b7-2992-4d1f-af16-7b8f0477b187
ms.tgt_platform: multiple
title: Creazione di script per oggetti helper
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 028079e49a2007d99b81f7832c4bce3cb016701d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309895"
---
# <a name="scripting-helper-objects"></a>Creazione di script per oggetti helper

WMI dispone di diversi oggetti helper di scripting che forniscono le conversioni richieste dagli script.

Gli oggetti helper di scripting WMI includono:

-   [**SWbemDateTime**](swbemdatetime.md)
-   [**SWbemObjectPath**](swbemobjectpath.md)
-   [**\_SecurityDescriptorHelper Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

Gli oggetti helper suddividono le strutture di dati compositi in modo che non sia necessario che uno script analizzi la struttura per ottenere le parti. La struttura DATETIME di **WMI** , ad esempio, non può essere visualizzata direttamente ed è diversa dalle altre strutture di dati DateTime di Windows, ad esempio **\_ Data VT**.

## <a name="swbemdatetime"></a>SWbemDateTime

L'oggetto [**SWbemDateTime**](swbemdatetime.md) fornisce proprietà che analizzano il giorno, il mese, l'anno, l'ora del giorno e così via. Fornisce inoltre metodi di conversione per convertire il valore DateTime Strumentazione gestione Windows (WMI) in e dai formati di **\_ Data** e [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) VT. Per le impostazioni di sicurezza di Internet Explorer (IE), l'oggetto **SWbemDateTime** è l'unico oggetto di scripting WMI contrassegnato come Safe per l'inizializzazione e sicuro per lo scripting. Per ulteriori informazioni ed esempi di conversioni di data e ora, vedere [date e ore](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) e l'articolo su TechNet ScriptCenter [it about time (Oh e about dates)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).

## <a name="swbemobjectpath"></a>SWbemObjectPath

Le proprietà di [**SWbemObjectPath**](swbemobjectpath.md) forniscono il percorso assoluto di un oggetto, ma suddividono anche le parti del percorso WMI, ad esempio server, spazio dei nomi, classe o percorso relativo. L'oggetto consente di impostare la sicurezza del percorso, ottenere i valori delle chiavi degli oggetti che rappresentano il percorso, determinare se un oggetto è un singleton e così via. Per ulteriori informazioni sull'utilizzo dei percorsi degli oggetti WMI, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).

## <a name="win32_securitydescriptorhelper"></a>\_SecurityDescriptorHelper Win32

La classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) converte il descrittore di sicurezza di un oggetto a protezione diretta da un formato a un altro.

Molti oggetti, ad esempio stampanti, spazi dei nomi WMI, chiavi del registro di sistema o applicazioni DCOM, dispongono di descrittori di sicurezza che controllano l'accesso all'oggetto. È possibile utilizzare WMI per individuare o modificare gli utenti che hanno accesso a questi oggetti ottenendo o impostando il descrittore di sicurezza associato all'oggetto.

Tuttavia, metodi diversi possono ottenere descrittori di sicurezza in una matrice di byte binaria, in formato SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-string-format) ) o come istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Il formato della matrice di byte binari di un descrittore di sicurezza non deve essere modificato, tranne nei metodi C++ progettati per [le operazioni del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-operations). I descrittori in SDDL sono stringhe, ma sono comunque difficili da modificare. Il formato più semplice da modificare è **Win32 \_ securityDescriptor**, perché contiene oggetti incorporati per il trustee, ACE e SID. Per ulteriori informazioni sulla struttura dei descrittori di sicurezza in WMI, vedere [oggetti del descrittore di sicurezza WMI](wmi-security-descriptor-objects.md). Per ulteriori informazioni su come eseguire le conversioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di script in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
