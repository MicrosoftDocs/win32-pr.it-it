---
description: WMI implementa una tecnica che consente l'archiviazione nel repository di più versioni localizzate della stessa classe.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localizzazione delle informazioni sulla classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348396"
---
# <a name="localizing-wmi-class-information"></a>Localizzazione delle informazioni sulla classe WMI

WMI implementa una tecnica che consente l'archiviazione nel repository di più versioni localizzate della stessa classe.

La definizione della classe è suddivisa nelle versioni seguenti:

-   Versione indipendente dalla lingua che contiene solo una definizione di classe di base.
-   Versione specifica del linguaggio che contiene informazioni localizzate, ad esempio descrizioni delle proprietà specifiche delle impostazioni locali.

Le definizioni delle classi specifiche del linguaggio vengono archiviate in uno spazio dei nomi figlio sotto lo spazio dei nomi che contiene una definizione di classe Basic indipendente dal linguaggio.

Quando si richiede una definizione di classe localizzata per le impostazioni locali specifiche, WMI combina la definizione della classe di base e le informazioni sulla classe localizzata per formare una classe localizzata completa. Per ottenere una versione localizzata di una classe WMI, è possibile specificare le impostazioni locali quando ci si connette a WMI e si imposta un flag che indica che si desiderano le informazioni localizzate. WMI quindi unisce le informazioni dalle versioni indipendenti dalla lingua e dalle versioni specifiche del linguaggio della definizione della classe per formare una classe localizzata.

Le classi WMI che contengono informazioni localizzate sono contrassegnate con il qualificatore della **modifica** e sono denominate classi modificate. una classe supporta le informazioni localizzate se dispone di questo qualificatore. È possibile determinare per quali impostazioni locali è stata localizzata la classe verificando la presenza di un altro qualificatore denominato [**impostazioni locali**](swbemobjectpath-locale.md). Il qualificatore delle impostazioni locali contiene un identificatore di localizzazione (LCID di Windows) che identifica le impostazioni locali. Ad esempio, le impostazioni locali per l'inglese americano sono 0x409. Se un qualificatore di una classe modificata contiene informazioni localizzate, contiene la versione del qualificatore **modificata** .

La localizzazione WMI include le attività seguenti:

-   [Creazione di definizioni di classi localizzate](creating-localized-class-definitions.md)
-   [Compilazione di file MOF localizzati](compiling-localized-mof-files.md)
-   [Localizzazione dei valori delle proprietà](localizing-property-values.md)
-   [Recupero di classi modificate](retrieving-amended-classes.md)

Per altre informazioni, vedere [considerazioni sulle classi modificate](amended-class-considerations.md).

 

 



