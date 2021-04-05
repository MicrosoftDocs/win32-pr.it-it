---
description: Un'applicazione di gestione che utilizza il provider del registro di sistema può definire classi con proprietà che rappresentano i dati del registro di sistema per chiavi specifiche e quindi archivia le classi nel repository WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definizione delle classi per il provider del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968054"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>Definizione delle classi per il provider del registro di sistema

Un'applicazione di gestione che utilizza il provider del registro di sistema può definire classi con proprietà che rappresentano i dati del registro di sistema per chiavi specifiche e quindi archivia le classi nel repository WMI. La maggior parte dei processi per la definizione di una classe per il registro di sistema è identica alla definizione di qualsiasi altra classe. Tuttavia, il provider del registro di sistema richiede l'utilizzo di tipi di dati e qualificatori specifici.

Nella procedura riportata di seguito viene descritto come definire una classe per il provider del registro di sistema.

**Per definire una classe per il provider del registro di sistema**

1.  Creare la classe come qualsiasi altra classe.

    Per ulteriori informazioni, vedere [creazione di una classe](creating-a-class.md).

2.  Eseguire il mapping dei tipi di dati del registro di sistema appropriati ai tipi WMI appropriati.

    Il provider registro di sistema esegue il mapping dei tipi di dati del registro di sistema a tipi di dati WMI specifici. Per ulteriori informazioni, vedere [mapping di un tipo di dati del registro di sistema a un tipo di dati WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).

3.  Utilizzare i qualificatori richiesti per definire il percorso del provider del registro di sistema e il percorso della chiave del registro di sistema appropriata.

    Il provider del registro di sistema usa tre qualificatori per definire il percorso di varie classi, provider e voci del registro di sistema. Per ulteriori informazioni, vedere [definizione di una classe Registry con qualificatori](defining-a-registry-class-with-qualifiers.md).

 

 



