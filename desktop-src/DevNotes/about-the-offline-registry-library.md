---
description: La libreria del Registro di sistema offline viene usata per modificare un hive del Registro di sistema all'esterno del Registro di sistema attivo.
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: Informazioni sulla libreria del Registro di sistema offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c2aecf71e8e42ad96c018bb613d7aac9a4a867bb301671e9553f1768a4ce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956180"
---
# <a name="about-the-offline-registry-library"></a>Informazioni sulla libreria del Registro di sistema offline

La libreria del Registro di sistema offline viene usata per modificare un hive del Registro di sistema all'esterno del Registro di sistema attivo.

La libreria del Registro di sistema offline è destinata agli scenari di aggiornamento del Registro di sistema, ad esempio la manutenzione di un'immagine del sistema operativo. Le funzioni del Registro di sistema offline offrono le funzionalità seguenti che non sono disponibili con le funzioni del Registro di sistema standard:

-   Le funzioni del Registro di sistema offline possono essere usate per modificare un hive del Registro di sistema in qualsiasi formato del Registro di sistema supportato. Le funzioni del Registro di sistema standard possono apportare modifiche solo a un hive del Registro di sistema attivo e le modifiche devono essere compatibili con la versione di Windows in esecuzione nel sistema.
-   La libreria del Registro di sistema offline richiede solo l'accesso in lettura per aprire un file hive del Registro di sistema e l'accesso in scrittura per salvare il file. Non vengono eseguiti altri controlli di accesso sugli oggetti nell'hive, rendendo possibile modificare l'hive con privilegi utente standard. Con le funzioni del Registro di sistema standard, il caricamento di un hive nel Registro di sistema attivo è un'operazione con privilegi che richiede l'accesso amministrativo.

Le funzioni del Registro di sistema offline non devono essere usate come sostituzione delle funzioni del Registro di sistema per i motivi seguenti:

-   Non è possibile condividere gli hive del Registro di sistema tra processi usando le funzioni del Registro di sistema offline.
-   Le funzioni del Registro di sistema offline usano un blocco semplice che può causare una grave riduzione delle prestazioni per le applicazioni multithreading.
-   Le modifiche apportate con le funzioni del Registro di sistema offline non vengono salvate fino a quando non viene chiamata la funzione [**ORSaveHive.**](orsavehive.md)

Le applicazioni non devono usare le funzioni del Registro di sistema offline per ignorare i requisiti di sicurezza del Registro di sistema. Per caricare un hive, un'applicazione in esecuzione senza i privilegi speciali richiesti dalla funzione [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) può usare la [funzione RegLoadAppKey.](/windows/win32/api/winreg/nf-winreg-regloadappkeya)

**Windows Server 2003 e Windows XP:** La [funzione RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) non è supportata.

Un *hive del Registro di* sistema offline è un hive del Registro di sistema caricato in memoria usando le funzioni del Registro di sistema offline. Per creare un hive del Registro di sistema offline vuoto, usare la [**funzione ORCreateHive.**](orcreatehive.md) Per modificare un hive del Registro di sistema esistente, usare la funzione [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) per salvare un hive dal Registro di sistema attivo in un file e quindi usare la funzione [**OROpenHive**](oropenhive.md) per aprire il file.

Le [**funzioni ORCreateHive**](orcreatehive.md) [**e OROpenHive**](oropenhive.md) restituiscono un handle alla chiave radice dell'hive del Registro di sistema offline. Questo handle può essere usato come handle per qualsiasi altra chiave nell'hive del Registro di sistema offline con le eccezioni seguenti: le funzioni [**ORCreateKey**](orcreatekey.md) e [**OROpenKey**](oropenkey.md) non possono essere usate per restituire un handle alla chiave radice. La [**funzione ORCloseKey**](orclosekey.md) non può essere usata per chiudere la chiave radice. e la [**funzione ORDeleteKey**](ordeletekey.md) non possono essere usate per eliminare la chiave radice. In tutti questi casi, la funzione ha esito negativo con **ERROR \_ INVALID \_ PARAMETER**.

Usare la [**funzione ORCreateKey**](orcreatekey.md) per aggiungere chiavi a un hive del Registro di sistema offline aperto e la [**funzione ORSetValue**](orsetvalue.md) per impostare i valori delle chiavi. La libreria del Registro di sistema offline supporta altre operazioni di base del Registro di sistema, ad esempio l'enumerazione, il recupero e l'eliminazione di chiavi e valori e l'impostazione di attributi chiave, ad esempio la sicurezza e il comportamento di virtualizzazione. Per un elenco di funzioni, vedere [Funzioni della libreria del Registro di sistema offline](offline-registry-library-functions.md).

Per salvare le modifiche apportate a un hive del Registro di sistema offline aperto, usare la [**funzione ORSaveHive**](orsavehive.md) per salvare l'hive in un file. Le modifiche non vengono mantenute a meno che **non venga chiamato ORSaveHive.** Dopo aver salvato l'hive, usare la [**funzione ORCloseHive**](orclosehive.md) per chiudere l'hive e liberare le risorse associate.

Un hive del Registro di sistema offline viene convalidato solo quando viene aperto usando la [**funzione OROpenHive.**](oropenhive.md) Se l'hive è danneggiato, l'operazione ha semplicemente esito negativo. non viene effettuato alcun tentativo di ripristinare l'hive. I controlli di accesso sugli oggetti nell'hive non vengono eseguiti fino a quando l'hive non viene caricato in un registro attivo con la [funzione RegLoadKey.](/windows/win32/api/winreg/nf-winreg-regloadkeya)

Le funzioni del Registro di sistema offline non supportano [le chiavi predefinite](../sysinfo/predefined-keys.md).

Tutte le stringhe di nome di chiave e valore passate alle funzioni del Registro di sistema offline devono essere Unicode.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni della libreria del Registro di \_ sistema offline](offline-registry-library-functions.md)
</dt> </dl>

 

 
