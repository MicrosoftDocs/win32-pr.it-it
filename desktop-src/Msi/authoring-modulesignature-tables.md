---
description: La tabella ModuleSignature contiene tutte le informazioni necessarie per identificare il modulo di merge.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Creazione di tabelle ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c7aaa84b7e5f2db2327bbb272d195333b7a82e609a2dfe2dc72b82eaad9bd09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045411"
---
# <a name="authoring-modulesignature-tables"></a>Creazione di tabelle ModuleSignature

La [tabella ModuleSignature contiene](modulesignature-table.md) tutte le informazioni necessarie per identificare il modulo di merge.

Il campo ModuleID è la chiave primaria per questa tabella e deve seguire la convenzione descritta in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md). Ad esempio, se il nome leggibile del modulo di unione è MyLibrary e il GUID per il modulo di unione è {880DE2F0-CDD8-11D1-A849-006097ABDE17}, La voce nella colonna ModuleID della tabella ModuleSignature diventa MyLibrary.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

Immettere l'identificatore decimale per la lingua predefinita del modulo di merge nel campo Lingua della tabella ModuleSignature.

Immettere la versione del modulo unione nel campo Versione.

 

 



