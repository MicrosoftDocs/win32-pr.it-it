---
description: Il codice sorgente per un'azione personalizzata di esempio denominata Launch, che soddisfa le specifiche di esempio, viene fornito da Windows Installer SDK come file Tutorial.cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Creazione dell'azione personalizzata di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536f22c95d871ab502518a0619efad5ae70cb348cdf75163fc50309b440f6393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045274"
---
# <a name="authoring-the-launch-custom-action"></a>Creazione dell'azione personalizzata di avvio

Il codice sorgente per un'azione personalizzata di esempio denominata Launch, che soddisfa le specifiche di esempio, viene fornito da Windows Installer SDK come file Tutorial.cpp. Questa azione personalizzata usa [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) per formattare una stringa contenente proprietà. La proprietà \[ \# FileKey \] viene risolta nel percorso completo del file HTML. Usare il file di origine per creare il file Tutorial.dll. Il punto di ingresso per questa DLL è LaunchTutorial.

L'azione personalizzata launch di esempio chiama una DLL scritta in C++ e viene generata da un flusso binario temporaneo. Le azioni personalizzate di questo tipo includono le costanti del tipo di base msidbCustomActionTypeDll e msidbCustomActionTypeBinaryData, che forniscono un tipo numerico di base uguale a 1. Vedere [Tipo di azione personalizzata 1.](custom-action-type-1.md) Poiché le specifiche richiedono che l'installazione continui se l'azione personalizzata ha esito negativo, Launch include anche la costante facoltativa **msidbCustomActionTypeContinue**, che è 64. Vedere [Opzioni di elaborazione per la restituzione di azioni personalizzate](custom-action-return-processing-options.md). Il tipo numerico totale di Launch è 65.

Continuare ad [aggiungere Launch alle tabelle CustomAction e Binary](adding-launch-to-the-customaction-and-binary-tables.md).

 

 



