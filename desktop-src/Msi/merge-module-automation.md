---
description: Mergemod.dll fornisce un oggetto COM che implementa le operazioni di merge e la generazione di immagini di origine per i moduli unione. L'oggetto principale implementa le interfacce per i programmi C/C++ e i client di automazione, Visual Basic e VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Automazione dei moduli di merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e592429b77671e154b932f3d79f6f57bb39a65ee2058aafd2164428234458acf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043051"
---
# <a name="merge-module-automation"></a>Automazione dei moduli di merge

Mergemod.dll fornisce un oggetto COM che implementa le operazioni di merge e la generazione di immagini di origine per i moduli unione. L'oggetto principale implementa le interfacce per i programmi C/C++ e i client di automazione, Visual Basic e VBScript.

Il metodo preferito per l'installazione Mergemod.dll è l'uso del Windows di installazione. L'ID componente per il componente che contiene l'interfaccia COM Mergemod.dll è {FD153241-37EC-11D2-8892-00A0C981B015}. Lo stesso file binario può essere usato in tutti Windows e la DLL verrà autoregistrato tramite regsvr32 nei sistemi meno recenti.

Si noti Mergemod.dll richiede che il Msvcrt.dll installato nel sistema.

Si noti Mergemod.dll 2.0 è necessario per creare [moduli unione configurabili.](configurable-merge-modules.md) Mergemod.dll versione 2.0 offre funzionalità estese in fase di compilazione tramite [**l'interfaccia IMsmMerge2.**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Questo CLSID supporta tutte le funzionalità esistenti [**dell'interfaccia IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) Mergemod.dll versione 1.0. L'interfaccia predefinita nell'oggetto [**Merge**](merge-object.md) Mergemod.dll 2.0 è l'interfaccia **IMsmMerge2** anziché l'interfaccia **IMsmMerge.**

[Modello a oggetti Mergemod.dll versione 1.0](object-model-for-mergemod-dll-version-1-0.md)

[Modello a oggetti per Mergemod.dll versione 2.0](object-model-for-mergemod-dll-version-2-0.md)

 

 
