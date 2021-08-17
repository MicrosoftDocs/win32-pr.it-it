---
description: WMI implementa una tecnica che consente di archiviare più versioni localizzate della stessa classe nel repository.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localizzazione delle informazioni sulle classi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3784128c48282d05620faf470217b195b26614d81b5b847e7a7a8ad6b9252f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131213"
---
# <a name="localizing-wmi-class-information"></a>Localizzazione delle informazioni sulle classi WMI

WMI implementa una tecnica che consente di archiviare più versioni localizzate della stessa classe nel repository.

La definizione della classe è suddivisa nelle versioni seguenti:

-   Versione indipendente dalla lingua che contiene solo una definizione di classe di base.
-   Versione specifica della lingua che contiene informazioni localizzate, ad esempio descrizioni di proprietà specifiche delle impostazioni locali.

Le definizioni di classe specifiche del linguaggio vengono archiviate in uno spazio dei nomi figlio sotto lo spazio dei nomi che contiene una definizione di classe di base indipendente dal linguaggio.

Quando si richiede una definizione di classe localizzata per impostazioni locali specifiche, WMI combina la definizione della classe di base e le informazioni sulla classe localizzata per formare una classe localizzata completa. È possibile ottenere una versione localizzata di una classe WMI specificando le impostazioni locali quando ci si connette a WMI e impostando un flag che indica che si desiderano informazioni localizzate. WMI unisce quindi le informazioni dalle versioni indipendenti dalla lingua e dalle versioni specifiche della lingua della definizione di classe per formare una classe localizzata.

Le classi WMI che contengono informazioni localizzate sono contrassegnate con il **qualificatore Di** rettifica e sono chiamate classi modificate; Una classe supporta le informazioni localizzate se dispone di questo qualificatore. È possibile determinare le impostazioni locali per cui è stata localizzata la classe controllando la presenza di un altro qualificatore denominato [**Locale.**](swbemobjectpath-locale.md) Il qualificatore delle impostazioni locali contiene un identificatore di localizzazione (Windows LCID) che identifica le impostazioni locali. Ad esempio, le impostazioni locali per l'inglese statunitense sono 0x409. Se un qualificatore in una classe modificata contiene informazioni localizzate, contiene il **qualificatore** corretto.

La localizzazione WMI include le attività seguenti:

-   [Creazione di definizioni di classi localizzate](creating-localized-class-definitions.md)
-   [Compilazione di file MOF localizzati](compiling-localized-mof-files.md)
-   [Localizzazione dei valori delle proprietà](localizing-property-values.md)
-   [Recupero di classi modificate](retrieving-amended-classes.md)

Per altre informazioni, vedere [Considerazioni sulle classi modificate.](amended-class-considerations.md)

 

 



