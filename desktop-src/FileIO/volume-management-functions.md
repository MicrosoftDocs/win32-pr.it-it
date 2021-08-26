---
description: Funzioni usate nella gestione dei volumi.
ms.assetid: dc985126-970c-49f2-877f-3759125e43b6
title: Funzioni di gestione dei volumi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3673e73007c977992d0209bcd79ded2afd4ed555ec3a22821e5f74d90e3cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130691"
---
# <a name="volume-management-functions"></a>Funzioni di gestione dei volumi

Funzioni usate nella gestione dei volumi.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew)<br/>                                   | Definisce, ridefinisce o elimina i nomi dei dispositivi MS-DOS.<br/>                                                                                                                |
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)<br/>                     | Elimina una lettera di unità o una cartella montata.<br/>                                                                                                                          |
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)<br/>                                   | Recupera il nome di un volume in un computer. <br/>                                                                                                                     |
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)<br/>               | Recupera il nome di una cartella montata nel volume specificato. <br/>                                                                                                   |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)<br/>                                     | Continua una ricerca di volumi avviata da una chiamata [**alla funzione FindFirstVolume.**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) <br/>                                                           |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)<br/>                 | Continua una ricerca nella cartella montata avviata da una chiamata alla [**funzione FindFirstVolumeMountPoint.**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) <br/>                               |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)<br/>                                   | Chiude l'handle di ricerca del volume specificato.<br/>                                                                                                                         |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)<br/>               | Chiude l'handle di ricerca della cartella montata specificato.<br/>                                                                                                                 |
| [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea)<br/>                                         | Determina se un'unità disco è rimovibile, fissa, CD-ROM, disco RAM o unità di rete.<br/>                                                                         |
| [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives)<br/>                                 | Recupera una maschera di bit che rappresenta le unità disco attualmente disponibili.<br/>                                                                                              |
| [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)<br/>                     | Riempie un buffer con stringhe che specificano unità valide nel sistema.<br/>                                                                                               |
| [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                         | Recupera informazioni sull'file system e sul volume associato alla directory radice specificata.<br/>                                                               |
| [**GetVolumeInformationByHandleW**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationbyhandlew)<br/>       | Recupera informazioni sull'file system e sul volume associati al file specificato.<br/>                                                                         |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)<br/> | Recupera un percorso **GUID del** volume associato al punto di montaggio del volume specificato (lettera di unità, percorso **GUID** del volume o cartella montata).<br/> |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)<br/>                               | Recupera il punto di montaggio del volume in cui è montato il percorso specificato.<br/>                                                                                              |
| [**GetVolumePathNamesForVolumeName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)<br/>   | Recupera un elenco di lettere di unità e percorsi di cartelle montate per il volume specificato.<br/>                                                                               |
| [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)<br/>                                     | Recupera informazioni sui nomi dei dispositivi MS-DOS.<br/>                                                                                                                   |
| [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)<br/>                                     | Imposta l'etichetta di un file system volume.<br/>                                                                                                                            |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)<br/>                           | Associa un volume a una lettera di unità o a una directory in un altro volume.<br/>                                                                                          |



 

Le funzioni seguenti vengono usate con i punti di montaggio del volume (lettere di unità, percorsi GUID del volume e cartelle montate).

-   [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)
-   [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)
-   [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)
-   [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)
-   [**GetVolumePathNamesForVolumeName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamesforvolumenamew)
-   [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)

 

 




