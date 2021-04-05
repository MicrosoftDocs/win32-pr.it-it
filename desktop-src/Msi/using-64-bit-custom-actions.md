---
description: Nei sistemi operativi a 64 bit Windows Installer possibile chiamare azioni personalizzate compilate per sistemi a 32 o 64 bit.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Uso di azioni personalizzate a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967899"
---
# <a name="using-64-bit-custom-actions"></a>Uso di azioni personalizzate a 64 bit

Nei sistemi operativi a 64 bit Windows Installer possibile chiamare azioni personalizzate compilate per sistemi a 32 o 64 bit. Un'azione personalizzata a 64 bit basata sugli [script](scripts.md) deve essere contrassegnata in modo esplicito come azione personalizzata a 64 bit aggiungendo il bit **msidbCustomActionType64BitScript** al tipo numerico dell'azione personalizzata nella colonna Type della [tabella CustomAction](customaction-table.md). Le azioni personalizzate basate su [file eseguibili](executable-files.md) o [librerie a collegamento dinamico](dynamic-link-libraries.md) conformi ai sistemi operativi a 64 bit non richiedono l'inclusione di questo bit aggiuntivo nella colonna Type della tabella CustomAction.

Per altre informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).

 

 



