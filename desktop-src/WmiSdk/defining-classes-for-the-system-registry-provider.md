---
description: Un'applicazione di gestione che usa il provider del Registro di sistema può definire classi con proprietà che rappresentano i dati del Registro di sistema per chiavi specifiche e quindi archivia le classi nel repository WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definizione di classi per il provider del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deecdbc419c5a245e609380732474a39089f28cb8c2fd76c2ac57546f2d00110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097291"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>Definizione di classi per il provider del Registro di sistema

Un'applicazione di gestione che usa il provider del Registro di sistema può definire classi con proprietà che rappresentano i dati del Registro di sistema per chiavi specifiche e quindi archivia le classi nel repository WMI. La maggior parte dei processi per la definizione di una classe per il Registro di sistema è identica alla definizione di qualsiasi altra classe. Tuttavia, il provider del Registro di sistema richiede l'uso di tipi di dati e qualificatori specifici.

La procedura seguente descrive come definire una classe per il provider del Registro di sistema.

**Per definire una classe per il provider del Registro di sistema**

1.  Creare la classe come qualsiasi altra classe.

    Per altre informazioni, vedere [Creazione di una classe](creating-a-class.md).

2.  Eseguire il mapping dei tipi di dati del Registro di sistema appropriati ai tipi WMI appropriati.

    Il provider del Registro di sistema esegue il mapping dei tipi di dati del Registro di sistema a tipi di dati WMI specifici. Per altre informazioni, vedere [Mapping di un tipo di dati del Registro di sistema a un tipo di dati WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).

3.  Usare i qualificatori necessari per definire il percorso del provider del Registro di sistema e il percorso della chiave del Registro di sistema appropriata.

    Il provider del Registro di sistema usa tre qualificatori per definire il percorso di varie classi, provider e voci del Registro di sistema. Per altre informazioni, vedere [Definizione di una classe Del Registro di sistema con qualificatori](defining-a-registry-class-with-qualifiers.md).

 

 



