---
description: Le funzioni di configurazione hardware recuperano informazioni quali processore, profilo hardware e informazioni sulla tastiera.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Configurazione hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee4abe543f0603ab6cf80ef395fe56e4e3300c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317660"
---
# <a name="hardware-configuration"></a>Configurazione hardware

Le funzioni di configurazione hardware recuperano informazioni quali processore, profilo hardware e informazioni sulla tastiera.

La funzione [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) recupera le informazioni sul processore e sulla memoria, ad esempio le dimensioni della pagina, l'identificatore OEM (Original Equipment Manufacturer), il numero e il tipo di processori, l'intervallo di indirizzi delle applicazioni e così via. La funzione [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) recupera informazioni sulle operazioni a virgola mobile e sui set di istruzioni supportati dal processore.

La funzione [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) recupera le informazioni sul profilo hardware. Il profilo hardware include informazioni quali lo stato di ancoraggio, l'identificatore univoco globale (GUID) e il nome visualizzato per il profilo. La funzione [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) recupera informazioni come il tipo di tastiera e il numero di tasti funzione sulla tastiera corrente.

 

 
