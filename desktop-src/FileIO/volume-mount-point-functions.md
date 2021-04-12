---
description: Funzioni utilizzate per gestire le cartelle montate.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funzioni cartella montata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346081"
---
# <a name="mounted-folder-functions"></a>Funzioni cartella montata

Le funzioni della cartella montata possono essere divise in tre gruppi, ovvero funzioni generiche, funzioni usate per analizzare i volumi e funzioni usate per analizzare un volume per le cartelle montate.

## <a name="general-purpose-mounted-folder-functions"></a>Funzioni della cartella montata General-Purpose



| Funzione                                                                     | Descrizione                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | Elimina una lettera di unità o una cartella montata.                                                                                                                   |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | Recupera il percorso GUID del volume associato al punto di montaggio del volume specificato (lettera di unità, percorso GUID volume o cartella montata). |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | Recupera la cartella montata associata al volume specificato.                                                                                  |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | Associa un volume a una lettera di unità o a una directory in un altro volume.                                                                                   |



 

## <a name="volume-scanning-functions"></a>Funzioni Volume-Scanning



| Funzione                                   | Descrizione                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | Restituisce il nome di un volume in un computer. [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) viene utilizzato per iniziare a enumerare i volumi di un computer. |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | Continua la ricerca di un volume avviata da una chiamata a [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).                                                     |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | Chiude una ricerca di volumi.                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>Funzioni di analisi della cartella montata



| Funzione                                                       | Descrizione                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | Recupera il nome di una cartella montata nel volume specificato. [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) viene utilizzato per iniziare l'analisi delle cartelle montate in un volume. |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | Continua la ricerca di una cartella montata avviata da una chiamata a [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).                                                                    |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | Chiude una ricerca di cartelle montate.                                                                                                                                                      |



 

 

 



