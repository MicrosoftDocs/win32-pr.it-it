---
description: La libreria del registro di sistema offline viene utilizzata per modificare un hive del registro di sistema all'esterno del registro di sistema attivo.
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: Informazioni sulla libreria del registro di sistema offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e08b401a4a77f55a54c48ad147bf38c8796472
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482853"
---
# <a name="about-the-offline-registry-library"></a>Informazioni sulla libreria del registro di sistema offline

La libreria del registro di sistema offline viene utilizzata per modificare un hive del registro di sistema all'esterno del registro di sistema attivo.

La libreria di registro offline è destinata agli scenari di aggiornamento del registro di sistema, come la manutenzione di un'immagine del sistema operativo. Le funzioni del registro di sistema offline forniscono le funzionalità seguenti che non sono disponibili con le funzioni standard del registro di sistema:

-   È possibile usare le funzioni del registro di sistema offline per modificare un hive del registro di sistema in qualsiasi formato di registro supportato. Le funzioni standard del registro di sistema possono apportare modifiche solo a un hive del registro di sistema attivo e le modifiche devono essere compatibili con la versione di Windows in esecuzione nel sistema.
-   La libreria del registro di sistema offline richiede solo l'accesso in lettura per aprire un file hive del registro di sistema e l'accesso in scrittura per salvare il file. Non vengono eseguiti altri controlli di accesso sugli oggetti in hive, rendendo possibile la modifica dell'hive con privilegi utente standard. Con le funzioni del registro di sistema standard, il caricamento di un hive nel registro di sistema attivo è un'operazione con privilegi che richiede l'accesso amministrativo.

Le funzioni del registro di sistema offline non devono essere utilizzate come sostituzioni per le funzioni del registro di sistema per i motivi seguenti:

-   Non è possibile condividere hive del registro di sistema tra processi usando le funzioni del registro di sistema offline.
-   Le funzioni del registro di sistema offline utilizzano un semplice blocco che può causare un peggioramento delle prestazioni per le applicazioni multithreading.
-   Le modifiche apportate con le funzioni del registro di sistema offline non vengono salvate fino a quando non viene chiamata la funzione [**ORSaveHive**](orsavehive.md) .

Le applicazioni non devono utilizzare le funzioni del registro di sistema offline per ignorare i requisiti di sicurezza del registro di sistema. Per caricare un hive, un'applicazione in esecuzione senza i privilegi speciali richiesti dalla funzione [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) può usare la funzione [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) .

**Windows Server 2003 e Windows XP:** La funzione [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) non è supportata.

Un *hive del registro di sistema offline* è un hive del registro di sistema che è stato caricato in memoria usando le funzioni del registro di sistema offline. Per creare un hive del registro di sistema offline vuoto, usare la funzione [**ORCreateHive**](orcreatehive.md) . Per modificare un hive del registro di sistema esistente, usare la funzione [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) per salvare un hive dal registro di sistema attivo in un file e quindi usare la funzione [**OROpenHive**](oropenhive.md) per aprire il file.

Le funzioni [**ORCreateHive**](orcreatehive.md) e [**OROpenHive**](oropenhive.md) restituiscono un handle alla chiave radice dell'hive del registro di sistema offline. Questo handle può essere usato come un handle per qualsiasi altra chiave nell'hive del registro di sistema offline con le eccezioni seguenti: non è possibile usare le funzioni [**ORCreateKey**](orcreatekey.md) e [**OROpenKey**](oropenkey.md) per restituire un handle alla chiave radice. Impossibile utilizzare la funzione [**ORCloseKey**](orclosekey.md) per chiudere la chiave radice. non è possibile usare la funzione [**ORDeleteKey**](ordeletekey.md) per eliminare la chiave radice. In tutti questi casi, la funzione ha esito negativo con **errore \_ \_ parametro non valido**.

Usare la funzione [**ORCreateKey**](orcreatekey.md) per aggiungere chiavi a un hive del registro di sistema offline aperto e la funzione [**ORSetValue**](orsetvalue.md) per impostare i valori delle chiavi. La libreria del registro di sistema offline supporta altre operazioni di base del registro di sistema, ad esempio l'enumerazione, il recupero e l'eliminazione di chiavi e valori, nonché l'impostazione di attributi chiave come il comportamento di sicurezza e virtualizzazione. Per un elenco di funzioni, vedere [funzioni della libreria del registro di sistema offline](offline-registry-library-functions.md).

Per salvare le modifiche apportate a un hive del registro di sistema offline aperto, usare la funzione [**ORSaveHive**](orsavehive.md) per salvare l'hive in un file. (Le modifiche non vengono mantenute a meno che non venga chiamato **ORSaveHive** ). Dopo aver salvato l'hive, usare la funzione [**ORCloseHive**](orclosehive.md) per chiudere l'hive e liberare le risorse associate.

Un hive del registro di sistema offline viene convalidato solo quando viene aperto tramite la funzione [**OROpenHive**](oropenhive.md) . Se l'hive è danneggiato, l'operazione ha esito negativo. non viene effettuato alcun tentativo di ripristino dell'hive. I controlli di accesso sugli oggetti nell'hive non vengono eseguiti fino a quando l'hive non viene caricato in un registro attivo con la funzione [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) .

Le funzioni del registro di sistema offline non supportano le [chiavi predefinite](../sysinfo/predefined-keys.md).

Tutte le stringhe del nome di chiave e valore passate alle funzioni del registro di sistema offline devono essere Unicode.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni della libreria del registro di sistema offline \_](offline-registry-library-functions.md)
</dt> </dl>

 

 
