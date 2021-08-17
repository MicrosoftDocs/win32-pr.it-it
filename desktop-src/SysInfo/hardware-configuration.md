---
description: Le funzioni di configurazione hardware recuperano informazioni quali processore, profilo hardware e tastiera.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Configurazione hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e396b2d08b489e92c7a407ca892250135fdd3d174d16de50d0c2d75428a88dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764419"
---
# <a name="hardware-configuration"></a>Configurazione hardware

Le funzioni di configurazione hardware recuperano informazioni quali processore, profilo hardware e tastiera.

La [**funzione GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) recupera le informazioni sul processore e sulla memoria, ad esempio le dimensioni della pagina, l'identificatore OEM (Original Equipment Manufacturer), il numero e il tipo di processori, l'intervallo di indirizzi dell'applicazione e così via. La [**funzione IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) recupera informazioni sulle operazioni a virgola mobile e sui set di istruzioni supportati dal processore.

La [**funzione GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) recupera informazioni sul profilo hardware. Il profilo hardware include informazioni quali lo stato di ancoraggio, l'identificatore univoco globale (GUID) e il nome visualizzato per il profilo. La [**funzione GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) recupera informazioni quali il tipo di tastiera e il numero di tasti funzione sulla tastiera corrente.

 

 
