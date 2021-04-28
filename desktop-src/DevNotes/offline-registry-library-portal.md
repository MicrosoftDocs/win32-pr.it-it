---
description: Libreria del Registro di sistema offline
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Libreria del Registro di sistema offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089249"
---
# <a name="offline-registry-library"></a>Libreria del Registro di sistema offline

## <a name="purpose"></a>Scopo

La libreria del Registro di sistema offline (Offreg.dll) viene usata per modificare un hive del Registro di sistema all'esterno del Registro di sistema attivo. Questa libreria è destinata agli scenari di aggiornamento del Registro di sistema, ad esempio la manutenzione di un'immagine del sistema operativo. La libreria supporta i formati hive del Registro di sistema a partire da Windows Vista.

## <a name="developer-audience"></a>Sviluppatori

Questa tecnologia è per i produttori di apparecchiature originali (OEM), i fornitori di software antivirus e antimalware e altri sviluppatori di applicazioni che devono essere in grado di analizzare i file hive del Registro di sistema senza caricarli nel Registro di sistema attivo.

## <a name="run-time-requirements"></a>Requisiti di runtime

La libreria del Registro di sistema offline viene fornita come libreria a collegamento dinamico (DLL) ridistribuibile binaria. Questa libreria viene eseguita nelle versioni seguenti di Windows:

<dl> Windows Server 2016  
Windows 10  
Windows 8.1  
Windows Server 2012 R2  
Windows 8  
Windows Server 2012  
Windows 7  
Windows Server 2008 R2  
Windows Server 2008  
Windows Vista  
</dl>

Le applicazioni devono collegarsi a Offreg.dll tramite il collegamento dinamico.

Offreg.dll viene fornito in Windows Driver Kit (WDK) (WDK) per Windows 10 e versioni precedenti del sistema operativo Windows.

Per informazioni su come ottenere wdk, vedere [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) (Come ottenere WDK e WLK) o visitare il sito Web delle sottoscrizioni [MSDN.](https://msdn.microsoft.com/subscriptions/default.aspx)

## <a name="in-this-section"></a>Contenuto della sezione

-   [**Informazioni sulla libreria del Registro di sistema offline**](about-the-offline-registry-library.md)
-   [**Funzioni della libreria del Registro di sistema offline**](offline-registry-library-functions.md)

 

 
