---
description: In ogni modulo unione è necessaria una tabella FeatureComponents vuota. Questa tabella vuota fornisce uno schema per lo strumento di unione se il file .msi di destinazione non dispone di una tabella FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Creazione di funzionalità del modulo unioneComponenti tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b2da3e25d84f4f10edad6566edeba5a10d43c5617340d40c733aa23d31f4b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650300"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Creazione di funzionalità del modulo unioneComponenti tabelle

In ogni modulo unione è necessaria una tabella [FeatureComponents](featurecomponents-table.md) vuota. Questa tabella vuota fornisce uno schema per lo strumento di unione se il file .msi di destinazione non dispone di una tabella FeatureComponents.

Se e solo se non è presente alcuna tabella FeatureComponents nel file di .msi di destinazione, lo strumento di merge usa la tabella vuota fornita nel modulo. In questo caso, lo strumento di unione crea una tabella duplicata nel file di .msi di destinazione e aggiunge righe che associano i nuovi componenti del modulo unione alle funzionalità del pacchetto di installazione dell'applicazione.

 

 



