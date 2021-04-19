---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Libreria del registro di sistema offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304562"
---
# <a name="offline-registry-library"></a>Libreria del registro di sistema offline

## <a name="purpose"></a>Scopo

La libreria del registro di sistema offline (Offreg.dll) viene usata per modificare un hive del registro di sistema all'esterno del registro di sistema attivo. Questa libreria è destinata agli scenari di aggiornamento del registro di sistema, come la manutenzione di un'immagine del sistema operativo. La libreria supporta i formati hive del registro di sistema a partire da Windows Vista.

## <a name="developer-audience"></a>Sviluppatori

Questa tecnologia è destinata agli OEM (Original Equipment Manufacturer), ai fornitori di software antivirus e antimalware e ad altri sviluppatori di applicazioni che devono essere in grado di analizzare i file hive del registro di sistema senza caricarli nel registro di sistema attivo.

## <a name="run-time-requirements"></a>Requisiti di runtime

La libreria del registro di sistema offline viene fornita come libreria di collegamento dinamico (DLL) ridistribuibile binario. Questa libreria viene eseguita nelle seguenti versioni di Windows:

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

Le applicazioni devono essere collegate a Offreg.dll tramite il collegamento dinamico.

Offreg.dll viene fornito in Windows Driver Kit (WDK) per Windows 10 e versioni precedenti del sistema operativo Windows.

Per informazioni su come ottenere il WDK, vedere [come ottenere WDK e WLK](/windows-hardware/drivers/download-the-wdk) oppure visitare il sito Web degli [abbonamenti MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .

## <a name="in-this-section"></a>Contenuto della sezione

-   [**Informazioni sulla libreria del registro di sistema offline**](about-the-offline-registry-library.md)
-   [**Funzioni della libreria del registro di sistema offline**](offline-registry-library-functions.md)

 

 
