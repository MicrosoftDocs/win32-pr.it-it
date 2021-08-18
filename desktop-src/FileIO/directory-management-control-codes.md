---
description: Codici di controllo usati con la compressione e la decompressione dei file e con reparse point.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Codici di controllo per la gestione della directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1354d1a4ce72f2867ece1f15218d9c7cb3f364a12ea3eb0d3b16f66b0954e89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755191"
---
# <a name="directory-management-control-codes"></a>Codici di controllo per la gestione della directory

I codici di controllo seguenti vengono usati con la [compressione e la decompressione dei file](file-compression-and-decompression.md).



| Codice di controllo                                             | Significato                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ GET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | Recupera lo stato di compressione corrente di un file o di una directory in un volume la cui file system supporta la compressione per flusso.<br/>    |
| [**FSCTL \_ SET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | Imposta lo stato di compressione di un file o di una directory in un volume la cui file system supporta la compressione per file e per directory.<br/> |



 

I codici di controllo seguenti vengono usati con [i reparse point](reparse-points.md).

## <a name="in-this-section"></a>Contenuto della sezione



| Codice di controllo                                                                   | Descrizione                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ DELETE \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | Elimina un reparse point dal file o dalla directory specificata.<br/>                                              |
| [**FSCTL \_ GET \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | Recupera i dati del reparse point associati al file o alla directory identificata dall'handle specificato.<br/> |
| [**FSCTL \_ SET \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | Imposta un reparse point in un file o in una directory.<br/>                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici di controllo della gestione dei file](file-management-control-codes.md)
</dt> <dt>

[Codici di controllo della gestione del volume](volume-management-control-codes.md)
</dt> </dl>

 

