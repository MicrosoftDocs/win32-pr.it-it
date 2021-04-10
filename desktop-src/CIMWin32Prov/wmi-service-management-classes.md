---
description: Le classi di gestione del servizio WMI vengono utilizzate per gestire il servizio WMI stesso e non il sistema del computer o la rete aziendale. La gestione di WMI comprende sia la configurazione del servizio WMI che la gestione delle operazioni WMI.
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: Classi di gestione del servizio WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126069"
---
# <a name="wmi-service-management-classes"></a>Classi di gestione del servizio WMI

Le classi di gestione del servizio WMI vengono utilizzate per gestire il servizio WMI stesso e non il sistema del computer o la rete aziendale. La gestione di WMI comprende sia la configurazione del servizio WMI che la gestione delle operazioni WMI.

La categoria Gestione del servizio WMI include le sottocategorie di classi seguenti:

-   [Classi di configurazione WMI](#wmi-configuration-classes)
-   [Classi di gestione WMI](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a>Classi di configurazione WMI

La classe di configurazione WMI deriva i metodi che configurano il servizio WMI.

Di seguito è riportata una tabella delle classi di configurazione WMI.



| Classe                                                             | Descrizione                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_MethodParameterClass Win32**](win32-methodparameterclass.md) | Classe di base astratta che implementa i parametri del metodo derivati da questa classe. |



 

## <a name="wmi-management-classes"></a>Classi di gestione WMI

Le classi di gestione WMI rappresentano i parametri operativi per il servizio WMI.

Di seguito è riportata una tabella delle classi di gestione WMI.



| Classe                                                       | Descrizione                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_WMISetting Win32**](win32-wmisetting.md)               | Contiene i parametri operativi per il servizio WMI.                                      |
| [**\_WMIElementSetting Win32**](win32-wmielementsetting.md) | Associazione tra un servizio in esecuzione nel sistema Windows e le impostazioni WMI che può utilizzare. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi Win32](./win32-provider.md)
</dt> </dl>

 

 
