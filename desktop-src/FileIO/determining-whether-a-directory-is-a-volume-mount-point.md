---
description: Come determinare se una directory specificata è una cartella montata.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Determinare se una directory è una cartella montata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884341"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a>Determinare se una directory è una cartella montata

È utile determinare se una directory è una cartella montata quando, ad esempio, si usa un'applicazione di backup o di ricerca limitata a un volume. Un'applicazione di questo tipo può raggiungere informazioni su più volumi se si usano funzioni come [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) per creare cartelle montate per gli altri volumi del volume a cui l'applicazione è limitata. Per ulteriori informazioni, vedere [creazione di cartelle montate](mounting-and-dismounting-a-volume.md).

Per determinare se una directory specificata è una cartella montata, chiamare prima la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ed esaminare il flag di **\_ \_ reparse \_ Point dell'attributo file** nel valore restituito per verificare se alla directory è associato un reparse point. In caso contrario, usare le funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) per ottenere il tag reparse nel membro **dwReserved0** della struttura di [**\_ \_ dati Find di Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) . Per determinare se il reparse point è una cartella montata (e non un'altra forma di punto di analisi), verificare se il valore del tag è uguale **al \_ \_ \_ \_ punto di montaggio del tag** di i/o del valore. Per ulteriori informazioni, vedere [reparse point](reparse-points.md).

Per ottenere il volume di destinazione di una cartella montata, usare la funzione [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .

In modo analogo, è possibile determinare se un reparse point è un collegamento simbolico verificando se il valore del tag è l'i/o di **\_ reparse \_ tag \_** simbolico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti di attributi file**](file-attribute-constants.md)
</dt> </dl>

 

 



