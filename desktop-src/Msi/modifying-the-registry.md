---
description: Le chiavi del Registro di sistema possono essere scritte nel Registro di sistema dopo l'installazione di tutti i componenti selezionati e dei file correlati.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modifica del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f1bd6145811097fcaf74f0622ac35412891d6aa0007c4411099ade6afddd36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082861"
---
# <a name="modifying-the-registry"></a>Modifica del Registro di sistema

Le chiavi del Registro di sistema possono essere scritte nel Registro di sistema dopo l'installazione di tutti i componenti selezionati e dei file correlati. Le azioni standard correlate alla modifica del Registro di sistema devono essere sequenziate dopo le azioni standard di installazione dei file perché le chiavi del Registro di sistema non possono essere scritte a meno che il componente e il file corrispondenti non siano stati installati correttamente.

[L'azione RegisterClassInfo](registerclassinfo-action.md) accede alla [tabella Class per](class-table.md) registrare le informazioni sulla classe COM dei componenti installati.

[L'azione RegisterExtensionInfo](registerextensioninfo-action.md) esegue una query sulla tabella [Extension](extension-table.md) e sulla [tabella Verb](verb-table.md) e registra le estensioni e le informazioni sui verbi di comando corrispondenti con il sistema operativo.

[L'azione RegisterProgIdInfo](registerprogidinfo-action.md) gestisce la registrazione delle informazioni sul ProgId OLE con il sistema operativo.

[L'azione RegisterMIMEInfo](registermimeinfo-action.md) elabora la tabella [MIME](mime-table.md) per registrare l'associazione tra un tipo di contesto MIME, l'estensione del nome file e il CLSID.

[L'azione WriteRegistryValues](writeregistryvalues-action.md) elabora la tabella [Registry](registry-table.md) e scrive le chiavi per tutti i componenti installati localmente o per l'esecuzione dall'origine. La tabella Registry consente la scrittura delle chiavi agli hive del Registro di sistema **HKEY \_ CLASSES \_ ROOT,** **HKEY \_ CURRENT \_ USER,** **HKEY LOCAL \_ \_ MACHINE** e **HKEY \_ USERS.**

[L'azione RemoveRegistryValues](removeregistryvalues-action.md) rimuove le chiavi contrassegnate per l'eliminazione nella colonna Name della tabella [Registry](registry-table.md) o [RemoveRegistry Table](removeregistry-table.md).

[L'azione RegisterTypeLibraries](registertypelibraries-action.md) elabora la tabella [TypeLib e](typelib-table.md) registra le librerie dei tipi installate con il sistema.

 

 



