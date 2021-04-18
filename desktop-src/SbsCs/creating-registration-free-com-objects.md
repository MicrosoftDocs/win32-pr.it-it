---
description: I contesti di attivazione consentono di usare oggetti COM senza che sia necessario registrarli.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Creazione di oggetti COM Registration-Free
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e377a04f44e6624294116b8274a8dcc1e82b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313756"
---
# <a name="creating-registration-free-com-objects"></a>Creazione di oggetti COM Registration-Free

I contesti di attivazione consentono di usare oggetti COM senza che sia necessario registrarli. In questo modo, l'applicazione deve disporre di più componenti con funzionalità diverse in base alla relativa versione anziché alle informazioni del registro di sistema. Più componenti possono esporre lo stesso oggetto COM con lo stesso GUID ma hanno funzionalità diverse in base alla versione.

Quando un'applicazione richiede un GUID da [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid), com cerca innanzitutto il mapping da ProgID a CLSID nel contesto di attivazione attiva. Quando un'applicazione utilizza [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un puntatore a interfaccia di istanza, com Cerca nel contesto di attivazione attiva per individuare quale dll ospiterà il CLSID. Se il contesto di attivazione non contiene le informazioni necessarie, COM cerca le informazioni nel registro di sistema usando il metodo usuale.

Si noti che poiché i contesti di attivazione sono per thread, COM esegue il marshalling del contesto di attivazione del thread di creazione al thread host e lo attiva prima di chiamare [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) nel thread host. Questa funzionalità è già presente in Windows, non è necessario che il codice client esegua alcuna operazione per implementarlo.

Le classi COM possono essere esportate da componenti ospitati senza passare attraverso il registro di sistema. Più componenti possono esporre lo stesso ProgID per oggetti COM diversi e l'applicazione host deve trovare solo il contesto di attivazione appropriato, quindi utilizzare [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere i puntatori all'interfaccia dell'oggetto host.

 

 
