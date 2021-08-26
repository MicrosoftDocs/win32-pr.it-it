---
description: Specifica di un contesto di attivazione predefinito
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: Specifica di un contesto di attivazione predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1598e0a111b358a783b940a5c036d63eef348740ff2467d3ed78720c6a5210
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977141"
---
# <a name="specifying-a-default-activation-context"></a>Specifica di un contesto di attivazione predefinito

Quando l'applicazione o il componente crea un nuovo processo, Windows un manifesto dell'applicazione predefinito. Si noti che un manifesto incluso come risorsa nell'applicazione ha la precedenza su un manifesto esterno. Il contesto di attivazione predefinito è il primo contesto di attivazione attivo prima dell'attivazione di qualsiasi altro contesto di attivazione. Questo contesto di attivazione è sempre attivo a meno che non si attivino altri contesti. Se si definisce ISOLATION AWARE ENABLED quando si compila l'applicazione o il componente, le chiamate come \_ \_ [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)e [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) possono eseguire la gestione automatica del contesto.

Il caricatore consente a un'applicazione di specificare il contesto di attivazione predefinito con due metodi. È possibile inserire il file manifesto nelle risorse del file eseguibile e il caricatore lo troverà. È uguale all'inserimento del file manifesto nella tabella delle risorse del file eseguibile. È possibile inserire il manifesto in un file denominato *Myapp*.exe. Manifesto nella stessa directory di *Myapp*.exe e il caricatore lo trova durante la ricerca *di Myapp*.exe.

Se non si usa nessuno di questi metodi, l'applicazione inizia con il contesto di attivazione predefinito del sistema, che contiene un set minimo di assembly.

Un modo migliore per usare la gestione automatica del contesto è compilare l'applicazione con ISOLATION \_ AWARE \_ ENABLED definito. Il metodo consigliato è impostare questo valore nella riga di comando del compilatore per l'intero progetto compilato anziché essere impostato in singoli file di origine o intestazioni. In questo modo la maggior parte delle API Win32 è a conoscenza dei contesti di attivazione e di come gestirli. Invece di dover eseguire la gestione del contesto di attivazione, è sufficiente inserire un manifesto nella tabella delle risorse nell'ID risorsa ISOLATIONAWARE MANIFEST RESOURCE ID (valore numerico 2), di tipo RT MANIFEST (valore numerico \_ \_ \_ \_ 24). Funzioni come [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)e [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) attivano quindi automaticamente questo contesto prima di effettuare la chiamata effettiva.

Si noti che se si esegue la compilazione con ISOLATION \_ AWARE \_ ENABLED definito, non è possibile eseguire la gestione del contesto di attivazione. Con ISOLATION AWARE ENABLED definito, Windows qualsiasi creazione dinamica del contesto di attivazione che l'applicazione potrebbe tentare di eseguire tra le chiamate \_ \_ [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) [**e CreateWindow.**](/windows/win32/api/winuser/nf-winuser-createwindowa) Ciò significa che quando l'applicazione usa ISOLATION AWARE ENABLED, è necessario assicurarsi che il manifesto contenga un elenco completo di tutti gli assembly necessari \_ \_ per il componente.

 

 
