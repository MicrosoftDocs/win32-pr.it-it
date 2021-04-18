---
description: Managed Object Format (MOF) è il linguaggio utilizzato per descrivere le classi Common Information Model (CIM).
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
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316564"
---
# <a name="managed-object-format-mof"></a>MOF (Managed Object Format)

Managed Object Format (MOF) è il linguaggio utilizzato per descrivere le classi [*Common Information Model (CIM)*](gloss-c.md) .

Il modo consigliato per i provider WMI di implementare nuove classi WMI è nei file MOF compilati utilizzando [**Mofcomp.exe**](mofcomp.md) nel [*repository WMI*](gloss-w.md). È anche possibile creare e modificare le classi e le istanze CIM usando l' [API com per WMI](com-api-for-wmi.md).

Un provider WMI è in genere costituito da un file MOF, che definisce i dati e le classi di evento per i quali il provider restituisce i dati e un file DLL contenente il codice che fornisce i dati. Per ulteriori informazioni, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).

Le applicazioni e gli script client WMI possono eseguire una query per le istanze delle classi MOF del provider o sottoscrivere la ricezione di notifiche degli eventi.

Con MOF è possibile eseguire le attività seguenti:

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

 

 



