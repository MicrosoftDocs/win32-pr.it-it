---
description: Codici di controllo usati con la compressione e la decompressione di file e con i reparse point.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Codici di controllo della gestione delle directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884338"
---
# <a name="directory-management-control-codes"></a>Codici di controllo della gestione delle directory

I codici di controllo seguenti vengono utilizzati con la [compressione e la decompressione di file](file-compression-and-decompression.md).



| Codice di controllo                                             | Significato                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_compressione FSCTL Get \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | Recupera lo stato di compressione corrente di un file o di una directory in un volume il cui file system supporta la compressione per flusso.<br/>    |
| [**\_compressione FSCTL set \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | Imposta lo stato di compressione di un file o di una directory in un volume il cui file system supporta la compressione per file e per directory.<br/> |



 

I codici di controllo seguenti vengono utilizzati con i [reparse point](reparse-points.md).

## <a name="in-this-section"></a>Contenuto della sezione



| Codice di controllo                                                                   | Descrizione                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ Elimina \_ punto di analisi \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | Elimina un reparse point dal file o dalla directory specificata.<br/>                                              |
| [**FSCTL \_ ottenere un \_ punto di analisi \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | Recupera i dati di reparse point associati al file o alla directory identificata dall'handle specificato.<br/> |
| [**FSCTL \_ set \_ reparse \_ Point**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | Imposta un reparse point su un file o una directory.<br/>                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici di controllo della gestione dei file](file-management-control-codes.md)
</dt> <dt>

[Codici di controllo della gestione del volume](volume-management-control-codes.md)
</dt> </dl>

 

