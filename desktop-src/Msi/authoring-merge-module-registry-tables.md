---
description: Utilizzare le tabelle del registro di sistema del modulo merge in base al tipo di informazioni del registro di sistema.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Creazione di tabelle del registro di sistema del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967267"
---
# <a name="authoring-merge-module-registry-tables"></a>Creazione di tabelle del registro di sistema del modulo merge

Utilizzare le tabelle del registro di sistema del modulo merge in base al tipo di informazioni del registro di sistema.

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a>TypeLib, Class, AppId, ProgId, estensione, verbo o tabelle MIME

Per le librerie dei tipi, le classi, le estensioni e i verbi, modificare le informazioni del registro di sistema nelle tabelle [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)o [MIME](mime-table.md) del modulo merge. Se si utilizza la [tabella del registro](registry-table.md) di sistema per aggiungere queste informazioni, Windows 2000 non è in grado di fornire un annuncio a livello di sistema per questi componenti.

Gli autori dei moduli merge possono decidere di non eseguire la registrazione utilizzando la tabella delle classi per i motivi seguenti:

-   Per essere registrato dalla tabella della classe, il file deve essere il percorso di base del relativo componente. Questa operazione potrebbe richiedere una modifica inaccettabile nell'organizzazione dei componenti.
-   Una chiamata COM può attivare il tentativo di reinstallare una classe annunciata da un programma di installazione. Gli autori possono decidere di non registrare una classe usando la tabella delle classi per evitare di attivare una reinstallazione quando il computer client non supporta un'interfaccia utente.

## <a name="registry-table"></a>Tabella del registro di sistema

Utilizzare la tabella del registro di sistema per aggiungere informazioni del registro di sistema che non possono essere create nelle tabelle TypeLib, Class, AppId, ProgId, Extension, verb o MIME. Windows 2000 non può fornire un annuncio a livello di sistema per i componenti che usano la tabella del registro di sistema.

Quando si crea la tabella del registro di sistema, fare riferimento ai percorsi dei file usando il \[ \# file \] o \[ . \]Formato di file anziché come \[ nome file della directory \] . Il secondo formato non supporta l'installazione dell'esecuzione dall'origine. Il primo formato rende inoltre più semplice rilevare i file mancanti e i componenti difettosi.

È necessario prestare attenzione quando si utilizza il testo formattato nella colonna chiave della tabella del registro di sistema. Poiché Windows Installer non reinstalla i componenti già installati, l'utilizzo di testo formattato in questo campo può causare la rimozione delle chiavi del registro di sistema durante la rimozione dell'applicazione.

## <a name="selfreg-table"></a>Tabella SelfReg

Non è consigliabile usare la tabella SelfReg. Per un elenco dei motivi per cui non si usa la registrazione automatica, vedere [tabella SelfReg](selfreg-table.md). È consigliabile utilizzare le tabelle TypeLib, Class, AppId, ProgId, Extension, verb e MIME, laddove possibile e la tabella del registro di sistema in tutti gli altri casi.

 

 



