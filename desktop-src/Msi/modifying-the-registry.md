---
description: È possibile scrivere chiavi del registro di sistema nel registro di sistema dopo aver installato tutti i componenti selezionati e i file correlati.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modifica del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348526"
---
# <a name="modifying-the-registry"></a>Modifica del registro di sistema

È possibile scrivere chiavi del registro di sistema nel registro di sistema dopo aver installato tutti i componenti selezionati e i file correlati. Le azioni standard relative alla modifica del registro di sistema devono essere sequenziate dopo le azioni standard di installazione dei file perché non è possibile scrivere chiavi del registro di sistema, a meno che il componente e il file corrispondenti non siano stati installati correttamente.

L' [azione RegisterClassInfo](registerclassinfo-action.md) accede alla [tabella della classe](class-table.md) per registrare le informazioni sulla classe com dei componenti installati.

L' [azione RegisterExtensionInfo](registerextensioninfo-action.md) esegue una query sulla [tabella di estensione](extension-table.md) e sulla [tabella dei verbi](verb-table.md) e registra le estensioni corrispondenti e le informazioni sui verbi di comando con il sistema operativo.

L' [azione RegisterProgIdInfo](registerprogidinfo-action.md) gestisce la registrazione delle informazioni OLE ProgID con il sistema operativo.

L' [azione RegisterMIMEInfo](registermimeinfo-action.md) elabora la [tabella MIME](mime-table.md) per registrare l'associazione tra un tipo di contesto MIME, l'estensione del nome del file e il CLSID.

L' [azione WriteRegistryValori consente](writeregistryvalues-action.md) elabora la [tabella del registro di sistema](registry-table.md) e scrive le chiavi per tutti i componenti installati localmente o per l'esecuzione dall'origine. La tabella del registro di sistema consente di scrivere chiavi **nella \_ \_ radice delle classi HKEY**, **HKEY \_ \_ utente corrente**, **HKEY \_ \_ computer locale** e **HKEY \_ gli** hive del registro di sistema.

L' [azione RemoveRegistryValues](removeregistryvalues-action.md) rimuove le chiavi contrassegnate per essere eliminate nella colonna Name della [tabella del registro di sistema](registry-table.md) o nella [tabella RemoveRegistry](removeregistry-table.md).

L' [azione RegisterTypeLibraries](registertypelibraries-action.md) elabora la [tabella TypeLib](typelib-table.md) e registra le librerie dei tipi installate nel sistema.

 

 



