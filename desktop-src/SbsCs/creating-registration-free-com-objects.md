---
description: I contesti di attivazione consentono di usare gli oggetti COM senza che sia necessario registrarli.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Creazione Registration-Free oggetti COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263d5a6c8160eaf15eba4eb799123e0e79d126ccd94b1d4a7a6d332bdb27dd51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142364"
---
# <a name="creating-registration-free-com-objects"></a>Creazione Registration-Free oggetti COM

I contesti di attivazione consentono di usare gli oggetti COM senza che sia necessario registrarli. In questo modo l'applicazione può avere più componenti con funzionalità diverse in base alla versione anziché alle informazioni del Registro di sistema. Più componenti possono esporre lo stesso oggetto COM con lo stesso GUID, ma hanno funzionalità diverse in base alla versione.

Quando un'applicazione richiede un GUID [**da CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid), COM cerca innanzitutto il mapping dal progid al CLSID nel contesto di attivazione attivo. Quando un'applicazione usa [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un puntatore di interfaccia dell'istanza, COM cerca nel contesto di attivazione attivo la DLL che ospiterà il CLSID. Se il contesto di attivazione non contiene le informazioni necessarie, COM cerca le informazioni nel Registro di sistema usando il metodo consueto.

Si noti che poiché i contesti di attivazione sono per thread, COM effettua il marshalling del contesto di attivazione del thread di creazione al thread host e lo attiva prima di chiamare [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) nel thread host. Questa funzionalità è già presente in Windows, il codice client non è necessario per implementare questa funzionalità.

Le classi COM possono essere esportate da componenti ospitati senza passare attraverso il Registro di sistema. Più componenti possono esporre lo stesso ProgID per oggetti COM diversi e l'applicazione host deve trovare solo il contesto di attivazione appropriato e quindi usare [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere i puntatori all'interfaccia dell'oggetto ospitato.

 

 
