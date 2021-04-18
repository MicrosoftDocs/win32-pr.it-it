---
description: Mergemod.dll fornisce un oggetto COM che implementa le operazioni di merge e la generazione dell'immagine di origine per i moduli unione. L'oggetto Main implementa le interfacce per i programmi C/C++ e i client di automazione, inclusi Visual Basic e VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Automazione del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319013"
---
# <a name="merge-module-automation"></a>Automazione del modulo merge

Mergemod.dll fornisce un oggetto COM che implementa le operazioni di merge e la generazione dell'immagine di origine per i moduli unione. L'oggetto Main implementa le interfacce per i programmi C/C++ e i client di automazione, inclusi Visual Basic e VBScript.

Il metodo preferito per l'installazione di Mergemod.dll consiste nell'utilizzare l'Windows Installer. L'ID componente per il componente che contiene il Mergemod.dll interfaccia COM è {FD153241-37EC-11D2-8892-00A0C981B015}. Lo stesso file binario può essere usato in tutti i sistemi Windows e la dll eseguirà la registrazione automatica tramite regsvr32 nei sistemi meno recenti.

Si noti che Mergemod.dll richiede l'installazione del Msvcrt.dll nel sistema.

Si noti che Mergemod.dll 2,0 è necessario per creare [moduli unione configurabili](configurable-merge-modules.md). Mergemod.dll versione 2,0 fornisce funzionalità estese in fase di compilazione tramite l'interfaccia [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) . Questo CLSID supporta tutte le funzionalità esistenti dell'interfaccia [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) fornita dalla versione Mergemod.dll 1,0. L'interfaccia predefinita nell'oggetto [**merge**](merge-object.md) di Mergemod.dll 2,0 è l'interfaccia **IMsmMerge2** invece dell'interfaccia **IMsmMerge** .

[Modello a oggetti per Mergemod.dll versione 1,0](object-model-for-mergemod-dll-version-1-0.md)

[Modello a oggetti per Mergemod.dll versione 2,0](object-model-for-mergemod-dll-version-2-0.md)

 

 
