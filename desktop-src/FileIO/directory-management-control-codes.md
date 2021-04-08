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
# <a name="directory-management-control-codes"></a><span data-ttu-id="c5594-103">Codici di controllo della gestione delle directory</span><span class="sxs-lookup"><span data-stu-id="c5594-103">Directory Management Control Codes</span></span>

<span data-ttu-id="c5594-104">I codici di controllo seguenti vengono utilizzati con la [compressione e la decompressione di file](file-compression-and-decompression.md).</span><span class="sxs-lookup"><span data-stu-id="c5594-104">The following control codes are used with [file compression and decompression](file-compression-and-decompression.md).</span></span>



| <span data-ttu-id="c5594-105">Codice di controllo</span><span class="sxs-lookup"><span data-stu-id="c5594-105">Control Code</span></span>                                             | <span data-ttu-id="c5594-106">Significato</span><span class="sxs-lookup"><span data-stu-id="c5594-106">Meaning</span></span>                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5594-107">**\_compressione FSCTL Get \_**</span><span class="sxs-lookup"><span data-stu-id="c5594-107">**FSCTL\_GET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | <span data-ttu-id="c5594-108">Recupera lo stato di compressione corrente di un file o di una directory in un volume il cui file system supporta la compressione per flusso.</span><span class="sxs-lookup"><span data-stu-id="c5594-108">Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.</span></span><br/>    |
| [<span data-ttu-id="c5594-109">**\_compressione FSCTL set \_**</span><span class="sxs-lookup"><span data-stu-id="c5594-109">**FSCTL\_SET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | <span data-ttu-id="c5594-110">Imposta lo stato di compressione di un file o di una directory in un volume il cui file system supporta la compressione per file e per directory.</span><span class="sxs-lookup"><span data-stu-id="c5594-110">Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression.</span></span><br/> |



 

<span data-ttu-id="c5594-111">I codici di controllo seguenti vengono utilizzati con i [reparse point](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="c5594-111">The following control codes are used with [reparse points](reparse-points.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5594-112">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c5594-112">In this section</span></span>



| <span data-ttu-id="c5594-113">Codice di controllo</span><span class="sxs-lookup"><span data-stu-id="c5594-113">Control Code</span></span>                                                                   | <span data-ttu-id="c5594-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5594-114">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5594-115">**FSCTL \_ Elimina \_ punto di analisi \_**</span><span class="sxs-lookup"><span data-stu-id="c5594-115">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | <span data-ttu-id="c5594-116">Elimina un reparse point dal file o dalla directory specificata.</span><span class="sxs-lookup"><span data-stu-id="c5594-116">Deletes a reparse point from the specified file or directory.</span></span><br/>                                              |
| [<span data-ttu-id="c5594-117">**FSCTL \_ ottenere un \_ punto di analisi \_**</span><span class="sxs-lookup"><span data-stu-id="c5594-117">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | <span data-ttu-id="c5594-118">Recupera i dati di reparse point associati al file o alla directory identificata dall'handle specificato.</span><span class="sxs-lookup"><span data-stu-id="c5594-118">Retrieves the reparse point data associated with the file or directory identified by the specified handle.</span></span><br/> |
| [<span data-ttu-id="c5594-119">**FSCTL \_ set \_ reparse \_ Point**</span><span class="sxs-lookup"><span data-stu-id="c5594-119">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | <span data-ttu-id="c5594-120">Imposta un reparse point su un file o una directory.</span><span class="sxs-lookup"><span data-stu-id="c5594-120">Sets a reparse point on a file or directory.</span></span><br/>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c5594-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5594-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5594-122">Codici di controllo della gestione dei file</span><span class="sxs-lookup"><span data-stu-id="c5594-122">File Management Control Codes</span></span>](file-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="c5594-123">Codici di controllo della gestione del volume</span><span class="sxs-lookup"><span data-stu-id="c5594-123">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

