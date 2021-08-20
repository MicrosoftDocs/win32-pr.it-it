---
description: Come determinare se una directory specificata è una cartella montata.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Determinare se una directory è una cartella montata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c0af53a63f64164604a5f8f22532add3dded1a46d19d96354c0da37e12d4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150594"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a>Determinare se una directory è una cartella montata

È utile determinare se una directory è una cartella montata quando, ad esempio, si usa un'applicazione di backup o di ricerca limitata a un volume. Un'applicazione di questo tipo può raggiungere informazioni su più volumi se si usano funzioni come [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) per creare cartelle montate per gli altri volumi nel volume a cui l'applicazione è limitata. Per altre informazioni, vedere [Creazione di cartelle montate.](mounting-and-dismounting-a-volume.md)

Per determinare se una directory specificata è una cartella montata, chiamare prima la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ed esaminare il flag **FILE ATTRIBUTE \_ \_ REPARSE \_ POINT** nel valore restituito per verificare se alla directory è associato un reparse point. In caso contrario, usare le funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) per ottenere il tag reparse nel membro **dwReserved0** della struttura [**\_ WIN32 FIND \_ DATA.**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Per determinare se il reparse point è una cartella montata (e non un'altra forma di reparse point), verificare se il valore del tag è uguale al valore **IO \_ REPARSE \_ TAG MOUNT \_ \_ POINT**. Per altre informazioni, vedere [Reparse point.](reparse-points.md)

Per ottenere il volume di destinazione di una cartella montata, usare la [**funzione GetVolumeNameForVolumeMountPoint.**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)

In modo analogo, è possibile determinare se un reparse point è un collegamento simbolico verificando se il valore del tag è **IO \_ REPARSE \_ TAG \_ SYMLINK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti di attributi file**](file-attribute-constants.md)
</dt> </dl>

 

 



