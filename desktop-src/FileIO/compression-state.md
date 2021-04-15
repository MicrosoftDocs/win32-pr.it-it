---
description: Ogni file e directory in un volume che supporta la compressione per singoli file e directory ha uno stato di compressione.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Stato di compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231755"
---
# <a name="compression-state"></a><span data-ttu-id="636e8-103">Stato di compressione</span><span class="sxs-lookup"><span data-stu-id="636e8-103">Compression State</span></span>

<span data-ttu-id="636e8-104">Ogni file e directory in un volume che supporta la compressione per singoli file e directory ha uno *stato di compressione*.</span><span class="sxs-lookup"><span data-stu-id="636e8-104">Each file and directory on a volume that supports compression for individual files and directories has a *compression state*.</span></span>

<span data-ttu-id="636e8-105">Mentre l'attributo di compressione di un file o di una directory indica semplicemente se il file o la directory è compresso o non compresso, lo stato di compressione specifica anche il formato di tutti i dati compressi.</span><span class="sxs-lookup"><span data-stu-id="636e8-105">Whereas the compression attribute of a file or directory indicates simply whether the file or directory is compressed or not compressed, the compression state also specifies the format of any compressed data.</span></span>

<span data-ttu-id="636e8-106">Usare il codice di controllo della [**\_ \_ compressione FSCTL Get**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) per determinare lo stato di compressione di un file o di una directory.</span><span class="sxs-lookup"><span data-stu-id="636e8-106">Use the [**FSCTL\_GET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) control code to determine the compression state of a file or directory.</span></span>

<span data-ttu-id="636e8-107">Lo stato di compressione è codificato come valore a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="636e8-107">Compression state is encoded as a 16-bit value.</span></span> <span data-ttu-id="636e8-108">Un valore dello stato di compressione del formato di compressione \_ \_ None indica che un file non è compresso.</span><span class="sxs-lookup"><span data-stu-id="636e8-108">A compression state value of COMPRESSION\_FORMAT\_NONE indicates that a file is not compressed.</span></span> <span data-ttu-id="636e8-109">Il valore predefinito per il formato di compressione \_ \_ indica che un file è compresso, usando il formato di compressione predefinito.</span><span class="sxs-lookup"><span data-stu-id="636e8-109">A value of COMPRESSION\_FORMAT\_DEFAULT indicates that a file is compressed, using the default compression format.</span></span> <span data-ttu-id="636e8-110">Qualsiasi altro valore indica che un file è compresso, usando il formato di compressione specificato dal valore dello stato di compressione.</span><span class="sxs-lookup"><span data-stu-id="636e8-110">Any other value indicates that a file is compressed, using the compression format specified by the compression state value.</span></span>

<span data-ttu-id="636e8-111">Usare il codice di controllo della [**\_ \_ compressione FSCTL set**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) per impostare lo stato di compressione di un file o di una directory.</span><span class="sxs-lookup"><span data-stu-id="636e8-111">Use the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code to set the compression state of a file or directory.</span></span> <span data-ttu-id="636e8-112">Questa operazione imposta anche l'attributo di compressione del file o della directory.</span><span class="sxs-lookup"><span data-stu-id="636e8-112">This operation also sets the compression attribute of the file or directory.</span></span>

<span data-ttu-id="636e8-113">L'impostazione dello stato di compressione di un file su un valore diverso da zero comprime il file, usando il formato di compressione codificato dal valore dello stato di compressione.</span><span class="sxs-lookup"><span data-stu-id="636e8-113">Setting the compression state of a file to a nonzero value compresses the file, using the compression format encoded by the compression state value.</span></span> <span data-ttu-id="636e8-114">Impostando lo stato di compressione di un file su zero, il file viene decompresso.</span><span class="sxs-lookup"><span data-stu-id="636e8-114">Setting a file's compression state to zero decompresses the file.</span></span> <span data-ttu-id="636e8-115">Si tratta di operazioni sincrone.</span><span class="sxs-lookup"><span data-stu-id="636e8-115">These are synchronous operations.</span></span> <span data-ttu-id="636e8-116">Il file viene compresso o decompresso immediatamente quando si imposta lo stato di compressione.</span><span class="sxs-lookup"><span data-stu-id="636e8-116">The file is compressed or decompressed immediately when you set its compression state.</span></span>

<span data-ttu-id="636e8-117">L'impostazione dello stato di compressione di una directory non provoca alcuna compressione o decompressione immediata.</span><span class="sxs-lookup"><span data-stu-id="636e8-117">Setting a directory's compression state does not cause any immediate compression or decompression.</span></span> <span data-ttu-id="636e8-118">Se invece si imposta lo stato di compressione di una directory, viene impostato uno stato di compressione predefinito che verrà assegnato a tutti i file e le sottodirectory appena creati.</span><span class="sxs-lookup"><span data-stu-id="636e8-118">Instead, setting a directory's compression state sets a default compression state that will be given to all newly created files and subdirectories.</span></span>

 

 
