---
description: Specifica di un contesto di attivazione predefinito
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: Specifica di un contesto di attivazione predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32cf0225a8e4290a09f7e6524a4b3ef47f9c4c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968302"
---
# <a name="specifying-a-default-activation-context"></a>Specifica di un contesto di attivazione predefinito

Quando l'applicazione o il componente crea un nuovo processo, Windows cerca un manifesto dell'applicazione predefinito. Si noti che un manifesto incluso come risorsa nell'applicazione ha la precedenza su un manifesto esterno. Il contesto di attivazione predefinito è il primo contesto di attivazione attivo prima che venga attivato un altro contesto di attivazione. Questo contesto di attivazione è sempre attivo, a meno che non si attivino altri contesti. Se si definisce \_ \_ Abilitazione dell'isolamento quando si compila l'applicazione o il componente, le chiamate come [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)e [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) possono eseguire la gestione automatica del contesto.

Il caricatore consente a un'applicazione di specificare il contesto di attivazione predefinito con due metodi. È possibile inserire il file manifesto nelle risorse dell'eseguibile e il caricatore lo troverà. Equivale a inserire il file manifesto nella tabella delle risorse dell'eseguibile. È possibile inserire il manifesto in un file denominato *MyApp*. exe. Manifesto nella stessa directory di *MyApp*. exe e il caricatore lo trova durante la ricerca di *MyApp*. exe.

Se non si utilizza nessuno di questi metodi, l'applicazione viene avviata con il contesto di attivazione predefinito del sistema, che contiene un set minimo di assembly.

Un modo migliore per utilizzare la gestione automatica del contesto consiste nel compilare l'applicazione con l'impostazione abilitata per l'isolamento \_ \_ . Il metodo consigliato consiste nell'impostare questa impostazione sulla riga di comando del compilatore per l'intero progetto da compilare anziché per l'impostazione di singoli file o intestazioni di origine. In questo modo, la maggior parte delle API Win32 è in grado di riconoscere i contesti di attivazione e come gestirli. Anziché dover eseguire la propria gestione del contesto di attivazione, è sufficiente inserire un manifesto nella tabella delle risorse all'ID risorsa ISOLATIONAWARE \_ \_ ID risorsa manifesto \_ (valore numerico 2), di tipo \_ manifesto RT (valore numerico 24). Funzioni come [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)e [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) attivano automaticamente questo contesto prima di effettuare la chiamata effettiva.

Si noti che se si \_ \_ esegue la compilazione con l'abilitazione dell'isolamento abilitata, non è possibile eseguire anche la gestione del contesto di attivazione. Con \_ \_ l'abilitazione dell'isolamento abilitato, Windows ignora qualsiasi creazione del contesto di attivazione dinamica che l'applicazione può tentare di eseguire tra le chiamate a [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) e [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) . Ciò significa che quando l'applicazione utilizza l' \_ isolamento \_ abilitato è necessario assicurarsi che il manifesto contenga un elenco completo di tutti gli assembly richiesti dal componente.

 

 
