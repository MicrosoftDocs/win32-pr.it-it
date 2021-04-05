---
description: Il codice sorgente per un'azione personalizzata di esempio denominata Launch, che soddisfa le specifiche di esempio, viene fornito dal Windows Installer SDK come file tutorial. cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Creazione dell'azione personalizzata di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967259"
---
# <a name="authoring-the-launch-custom-action"></a>Creazione dell'azione personalizzata di avvio

Il codice sorgente per un'azione personalizzata di esempio denominata Launch, che soddisfa le specifiche di esempio, viene fornito dal Windows Installer SDK come file tutorial. cpp. Questa azione personalizzata USA [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) per formattare una stringa che contiene le proprietà. La proprietà \[ \# FileKey viene \] risolta nel percorso completo del file HTML. Usare il file di origine per creare il file Tutorial.dll. Il punto di ingresso per questa DLL è LaunchTutorial.

L'avvio dell'azione personalizzata di esempio chiama una DLL scritta in C++ e viene generata da un flusso binario temporaneo. Le azioni personalizzate di questo tipo includono le costanti del tipo di base msidbCustomActionTypeDll e msidbCustomActionTypeBinaryData, che assegnano un tipo numerico di base uguale a 1. Vedere [azione personalizzata di tipo 1](custom-action-type-1.md). Poiché le specifiche richiedono che l'installazione continui se l'azione personalizzata ha esito negativo, Launch include anche la costante facoltativa **msidbCustomActionTypeContinue**, che è 64. Vedere [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md). Il tipo numerico totale di avvio è 65.

Continuare ad [aggiungere Launch alle tabelle CustomAction e Binary](adding-launch-to-the-customaction-and-binary-tables.md).

 

 



