---
description: Managed Object Format (MOF) è il linguaggio usato per descrivere Common Information Model (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: MOF (Managed Object Format)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ac36bd89979d6cf0de0a4d574a47a6ce7060f90e5577402eba77aa2de42bbedb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131179"
---
# <a name="managed-object-format-mof"></a>MOF (Managed Object Format)

Managed Object Format (MOF) è il linguaggio usato per descrivere Common Information Model [*(CIM).*](gloss-c.md)

Il modo consigliato per i provider WMI per implementare nuove classi WMI è nei file MOF che vengono compilatiMofcomp.exe [**nel**](mofcomp.md) [*repository WMI*](gloss-w.md). È anche possibile creare e modificare classi e istanze CIM usando [l'API COM per WMI.](com-api-for-wmi.md)

Un provider WMI è in genere costituito da un file MOF, che definisce i dati e le classi di evento per cui il provider restituisce i dati, e da un file DLL che contiene il codice che fornisce i dati. Per altre informazioni, vedere [Fornire dati a WMI.](providing-data-to-wmi.md)

Le applicazioni e gli script client WMI possono eseguire query per le istanze delle classi MOF del provider o sottoscrivere per ricevere notifiche degli eventi.

È possibile eseguire le attività seguenti con MOF:

-   [Compilazione di file MOF](compiling-mof-files.md)
-   [Creazione di una classe](creating-a-class.md)
-   [Creazione di un'istanza](creating-an-instance.md)
-   [Creazione di un metodo](creating-a-method.md)
-   [Aggiunta di un qualificatore](adding-a-qualifier.md)
-   [Creazione di un commento](creating-a-comment.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> </dl>

 

 



