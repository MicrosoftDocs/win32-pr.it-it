---
description: Usare le tabelle del Registro di sistema del modulo merge in base al tipo di informazioni del Registro di sistema.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Creazione di tabelle del Registro di sistema del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03726481905d4efee2405d0b383f53833d840090fea74e2d41fc6ae67a8e5bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066151"
---
# <a name="authoring-merge-module-registry-tables"></a>Creazione di tabelle del Registro di sistema del modulo merge

Usare le tabelle del Registro di sistema del modulo merge in base al tipo di informazioni del Registro di sistema.

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a>Tabelle TypeLib, Class, AppId, ProgId, Extension, Verbo o MIME

Per librerie dei tipi, classi, estensioni e verbi, creare le informazioni del Registro di sistema nelle tabelle [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verbo](verb-table.md) [o MIME del modulo merge.](mime-table.md) Se si usa la [tabella Registry per](registry-table.md) aggiungere queste informazioni, Windows 2000 non è in grado di fornire annunci a livello di sistema per questi componenti.

Gli autori di moduli unione possono decidere di non eseguire la registrazione usando la tabella Class per i motivi seguenti:

-   Per essere registrato dalla tabella Class, il file deve essere il KeyPath del relativo componente. Ciò potrebbe richiedere una modifica inaccettabile nell'organizzazione dei componenti.
-   Una chiamata COM può attivare un tentativo di installazione di reinstallare una classe annunciata. Gli autori possono decidere di non registrare una classe usando la tabella Class per evitare di attivare una reinstallazione quando il computer client non supporta un'interfaccia utente.

## <a name="registry-table"></a>Tabella del Registro di sistema

Usare la tabella Registry per aggiungere informazioni del Registro di sistema che non possono essere scritte nelle tabelle TypeLib, Class, AppId, ProgId, Extension, Verbo o MIME. Windows 2000 non è in grado di fornire annunci a livello di sistema per i componenti che usano la tabella Del Registro di sistema.

Quando si crea la tabella Registry, fare riferimento ai percorsi dei file usando \[ \# il file o \] \[ ! Formato \] di file anziché nome file della \[ \] directory. Quest'ultimo formato non supporta l'installazione dall'origine. Il primo formato rende anche più facile rilevare i file mancanti e i componenti difettosi.

È necessario fare attenzione quando si usa testo formattato nella colonna Chiave della tabella Registro di sistema. Poiché Windows installer non reinstalla i componenti già installati, l'uso di testo formattato in questo campo può causare la rimozione delle chiavi del Registro di sistema.

## <a name="selfreg-table"></a>Tabella SelfReg

Non è consigliabile usare la tabella SelfReg. Per un elenco dei motivi per cui non si usa la registrazione automatica, vedere [la tabella SelfReg](selfreg-table.md). È consigliabile usare le tabelle TypeLib, Class, AppId, ProgId, Extension, Verb e MIME, dove possibile, e la tabella Registry in tutti gli altri casi.

 

 



