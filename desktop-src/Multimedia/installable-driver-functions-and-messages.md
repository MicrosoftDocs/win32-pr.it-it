---
title: Funzioni e messaggi installabili dei driver
description: Funzioni e messaggi installabili dei driver
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- driver installabili, funzioni
- driver installabili, messaggi
- driver installabili, funzione OpenDriver
- Funzione OpenDriver
- driver installabili,messaggi personalizzati
- messaggi del driver
- messaggi di driver personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3afe479d242e0c1a8821812566267343b54975ae1701dd987ac65166061f2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987084"
---
# <a name="installable-driver-functions-and-messages"></a>Funzioni e messaggi installabili dei driver

È possibile aprire un driver installabile da un'applicazione usando la [**funzione OpenDriver.**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) Questa funzione crea un'istanza del driver, carica il driver in memoria se non esiste un'altra istanza e restituisce l'handle della nuova istanza. Quando si apre un driver installabile, è necessario specificare il percorso completo del driver o i nomi della chiave del Registro di sistema e del valore associati al driver.

Una volta aperto un driver, è possibile indirizzarlo all'esecuzione di attività usando la [**funzione SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) per inviare i messaggi del driver al driver. Ad esempio, è possibile indirizzare il driver per visualizzare la finestra di dialogo di configurazione inviando il [**DRV \_ CONFIGURE**](drv-configure.md) messaggio. Prima di inviare questo messaggio, è necessario determinare se il driver dispone di una finestra di dialogo di configurazione inviando il messaggio [**\_ DRV QUERYCONFIGURE**](drv-queryconfigure.md) e verificando la presenza di un valore restituito diverso da zero. Molti driver forniscono un set di messaggi personalizzati che è possibile inviare per indirizzare le operazioni del driver.

Se è necessario un accesso speciale a un driver installabile, ad esempio l'accesso alle relative risorse, è possibile recuperare l'handle di modulo del driver usando la [**funzione GetDriverModuleHandle.**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)

Quando il driver installabile non è più necessario, è possibile chiuderlo usando la [**funzione CloseDriver.**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver)

È possibile usare le funzioni e i messaggi del driver installabili per aprire e gestire qualsiasi driver installabile. Tuttavia, la linea di azione consigliata per l'apertura e la gestione dei dispositivi multimediali è usare prima di tutto i servizi standard ( ad esempio [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)e [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) per i dispositivi di output waveform), se presenti. Se non esistono servizi standard per un driver multimediale, aprire e gestire il driver usando le funzioni e i messaggi installabili del driver.

> [!Note]  
> Le [**funzioni SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) e [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) sono le funzioni preferite da usare per inviare messaggi a un driver e per ottenere un handle per un'istanza del modulo. La funzione [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) precedente, tuttavia, è stata inclusa per mantenere la compatibilità con le versioni precedenti del Windows operativo.

 

 

 