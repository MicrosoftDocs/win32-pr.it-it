---
description: La tabella ModuleSignature contiene tutte le informazioni necessarie per identificare il modulo merge.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Creazione di tabelle ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311038"
---
# <a name="authoring-modulesignature-tables"></a>Creazione di tabelle ModuleSignature

La [tabella ModuleSignature](modulesignature-table.md) contiene tutte le informazioni necessarie per identificare il modulo merge.

Il campo ModuleID è la chiave primaria per questa tabella e deve seguire la convenzione descritta in [denominazione delle chiavi primarie nei database dei moduli di Unione](naming-primary-keys-in-merge-module-databases.md). Se, ad esempio, il nome leggibile del modulo merge è MyLibrary e il GUID del modulo merge è {880DE2F0-CDD8-11D1-A849-006097ABDE17}, la voce nella colonna ModuleID della tabella ModuleSignature diventa MyLibrary. 880DE2F0 CDD8 11D1 A849 006097ABDE17 \_ \_ \_ \_ .

Immettere l'identificatore decimale per la lingua predefinita del modulo merge nel campo Language della tabella ModuleSignature.

Immettere la versione del modulo merge nel campo versione.

 

 



