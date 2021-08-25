---
description: Funzioni usate per gestire le cartelle montate.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funzioni per le cartelle montate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13175dc4846d8f8438a3f1b94b3e407aaf347e2b6d10ad5c3761899882ecdfaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870781"
---
# <a name="mounted-folder-functions"></a>Funzioni per le cartelle montate

Le funzioni delle cartelle montate possono essere suddivise in tre gruppi: funzioni per utilizzo generico, funzioni usate per l'analisi dei volumi e funzioni usate per analizzare un volume per le cartelle montate.

## <a name="general-purpose-mounted-folder-functions"></a>General-Purpose funzioni per le cartelle montate



| Funzione                                                                     | Descrizione                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Elimina una lettera di unità o una cartella montata.                                                                                                                   |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Recupera il percorso GUID del volume associato al punto di montaggio del volume specificato (lettera di unità, percorso GUID del volume o cartella montata). |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Recupera la cartella montata associata al volume specificato.                                                                                  |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Associa un volume a una lettera di unità o a una directory in un altro volume.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Volume-Scanning funzioni



| Funzione                                   | Descrizione                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Restituisce il nome di un volume in un computer. [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) viene usato per iniziare a enumerare i volumi di un computer. |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Continua una ricerca di volumi avviata da una [**chiamata a FindFirstVolume.**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)                                                     |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Chiude una ricerca di volumi.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Funzioni di analisi delle cartelle montate



| Funzione                                                       | Descrizione                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Recupera il nome di una cartella montata nel volume specificato. [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) viene usato per avviare l'analisi delle cartelle montate in un volume. |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Continua una ricerca di cartelle montate avviata da una chiamata a [**FindFirstVolumeMountPoint.**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)                                                                    |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Chiude una ricerca di cartelle montate.                                                                                                                                                      |



 

 

 



