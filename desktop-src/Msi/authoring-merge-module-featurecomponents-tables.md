---
description: In ogni modulo merge è necessaria una tabella FeatureComponents vuota. Questa tabella vuota fornisce uno schema per lo strumento di merge se il file con estensione msi di destinazione non dispone di una propria tabella FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Creazione di tabelle FeatureComponents del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3522f32f91a66df93e9096bf9c528f8d00e11f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311044"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Creazione di tabelle FeatureComponents del modulo merge

In ogni modulo merge è necessaria una [tabella FeatureComponents](featurecomponents-table.md) vuota. Questa tabella vuota fornisce uno schema per lo strumento di merge se il file con estensione msi di destinazione non dispone di una propria tabella FeatureComponents.

Se e solo se non è presente alcuna tabella FeatureComponents nel file con estensione msi di destinazione, lo strumento di merge usa la tabella vuota fornita nel modulo. In questo caso, lo strumento di merge crea una tabella duplicata nel file con estensione msi di destinazione e aggiunge righe che associano i nuovi componenti del modulo merge alle funzionalità del pacchetto di installazione dell'applicazione.

 

 



