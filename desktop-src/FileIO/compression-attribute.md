---
description: In un volume file system NTFS ogni file e directory dispone di un attributo di compressione.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Attributo Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885737"
---
# <a name="compression-attribute"></a><span data-ttu-id="fb10f-103">Attributo Compression</span><span class="sxs-lookup"><span data-stu-id="fb10f-103">Compression Attribute</span></span>

<span data-ttu-id="fb10f-104">In un volume file system NTFS ogni file e directory dispone di un *attributo di compressione*.</span><span class="sxs-lookup"><span data-stu-id="fb10f-104">On an NTFS file system volume, each file and directory has a *compression attribute*.</span></span> <span data-ttu-id="fb10f-105">Altri file System possono implementare anche un attributo di compressione per singoli file e directory.</span><span class="sxs-lookup"><span data-stu-id="fb10f-105">Other file systems may also implement a compression attribute for individual files and directories.</span></span>

<span data-ttu-id="fb10f-106">È possibile determinare se un file system supporta un attributo di compressione per file e directory chiamando la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminando il flag di bit di **\_ \_ compressione del file di file** .</span><span class="sxs-lookup"><span data-stu-id="fb10f-106">You can determine whether a file system supports a compression attribute for files and directories by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_FILE\_COMPRESSION** bit flag.</span></span>

<span data-ttu-id="fb10f-107">Utilizzare la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) o [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) per determinare l'attributo di compressione di un file o di una directory.</span><span class="sxs-lookup"><span data-stu-id="fb10f-107">Use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function to determine the compression attribute of a file or directory.</span></span>

<span data-ttu-id="fb10f-108">Se è impostato l'attributo di compressione di un file (**\_ attributo file \_ compresso**), tutti i dati nel file vengono compressi.</span><span class="sxs-lookup"><span data-stu-id="fb10f-108">If a file's compression attribute is set (**FILE\_ATTRIBUTE\_COMPRESSED**), all data in the file is compressed.</span></span> <span data-ttu-id="fb10f-109">Se l'attributo è chiaro, nessuno dei dati nel file viene compresso.</span><span class="sxs-lookup"><span data-stu-id="fb10f-109">If the attribute is clear, none of the data in the file is compressed.</span></span> <span data-ttu-id="fb10f-110">Non esiste alcuno stato parzialmente compresso da un punto di vista della programmazione in modalità utente; l'attributo Compression è un semplice indicatore booleano dello stato di compressione.</span><span class="sxs-lookup"><span data-stu-id="fb10f-110">There is no partially compressed state from a user-mode programming perspective; the compression attribute is a simple Boolean indicator of compression state.</span></span>

<span data-ttu-id="fb10f-111">L'attributo di compressione di una directory fornisce un attributo di compressione predefinito per i file e le sottodirectory appena creati.</span><span class="sxs-lookup"><span data-stu-id="fb10f-111">A directory's compression attribute provides a default compression attribute for newly created files and subdirectories.</span></span> <span data-ttu-id="fb10f-112">Quando si chiama [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) per creare un nuovo file o una nuova directory, il nuovo file o la nuova directory eredita l'attributo di compressione della relativa directory padre.</span><span class="sxs-lookup"><span data-stu-id="fb10f-112">When you call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) to create a new file or directory, the new file or directory inherits the compression attribute of its parent directory.</span></span>

<span data-ttu-id="fb10f-113">Per modificare l' **attributo \_ \_ compresso dell'attributo file** per un file o una directory, è necessario usare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con il codice di controllo della [**\_ \_ compressione FSCTL set**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .</span><span class="sxs-lookup"><span data-stu-id="fb10f-113">To modify the **FILE\_ATTRIBUTE\_COMPRESSED** attribute for a file or directory, you must use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb10f-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb10f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb10f-115">**Costanti di attributi file**</span><span class="sxs-lookup"><span data-stu-id="fb10f-115">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 
