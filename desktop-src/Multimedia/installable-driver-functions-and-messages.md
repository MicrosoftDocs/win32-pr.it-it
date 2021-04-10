---
title: Messaggi e funzioni driver installabili
description: Messaggi e funzioni driver installabili
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- driver installabili, funzioni
- driver installabili, messaggi
- driver installabili, funzione OpenDriver
- OpenDriver (funzione)
- driver installabili, messaggi personalizzati
- messaggi driver
- messaggi di driver personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963043"
---
# <a name="installable-driver-functions-and-messages"></a>Messaggi e funzioni driver installabili

È possibile aprire un driver installabile da un'applicazione tramite la funzione [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) . Questa funzione crea un'istanza del driver, caricando il driver in memoria se non esiste nessun'altra istanza e restituisce l'handle della nuova istanza. Quando si apre un driver installabile, è necessario specificare il percorso completo del driver o i nomi della chiave del registro di sistema e il valore associato al driver.

Quando un driver è aperto, è possibile indirizzarlo per eseguire attività usando la funzione [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) per inviare messaggi di driver al driver. Ad esempio, è possibile indicare al driver di visualizzare la relativa finestra di dialogo di configurazione inviando il messaggio di configurazione [**drv \_**](drv-configure.md) . Prima di inviare questo messaggio, è necessario determinare se il driver dispone di una finestra di dialogo di configurazione inviando il messaggio [**drv \_ QUERYCONFIGURE**](drv-queryconfigure.md) e verificando la presenza di un valore restituito diverso da zero. Molti driver forniscono un set di messaggi personalizzati che è possibile inviare per indirizzare le operazioni del driver.

Se è necessario un accesso speciale a un driver installabile, ad esempio l'accesso alle risorse, è possibile recuperare l'handle del modulo del driver usando la funzione [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) .

Quando il driver installabile non è più necessario, è possibile chiuderlo utilizzando la funzione [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) .

Per aprire e gestire qualsiasi driver installabile, è possibile utilizzare le funzioni e i messaggi di driver installabili. Tuttavia, la linea di azione consigliata per l'apertura e la gestione dei dispositivi multimediali consiste nel usare prima i servizi standard, ad esempio [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)e [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) per i dispositivi di output della forma d'onda, se esistenti. Se per un driver multimediale non esistono servizi standard, aprire e gestire il driver utilizzando le funzioni e i messaggi di driver installabili.

> [!Note]  
> Le funzioni [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) e [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) sono le funzioni preferite da usare per inviare messaggi a un driver e ottenere un handle per un'istanza del modulo. È stata tuttavia inclusa la funzione [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) precedente, che consente di mantenere la compatibilità con le versioni precedenti del sistema operativo Windows.

 

 

 