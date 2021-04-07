---
description: Rappresenta un attributo del nome di file. Un file ha un attributo di nome file per ogni directory in cui viene immesso.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Struttura FILE_NAME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049085"
---
# <a name="file_name-structure"></a><span data-ttu-id="97334-104">\_Struttura del nome file</span><span class="sxs-lookup"><span data-stu-id="97334-104">FILE\_NAME structure</span></span>

<span data-ttu-id="97334-105">\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]</span><span class="sxs-lookup"><span data-stu-id="97334-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="97334-106">Rappresenta un attributo del nome di file.</span><span class="sxs-lookup"><span data-stu-id="97334-106">Represents a file name attribute.</span></span> <span data-ttu-id="97334-107">Un file ha un attributo di nome file per ogni directory in cui viene immesso.</span><span class="sxs-lookup"><span data-stu-id="97334-107">A file has one file name attribute for every directory it is entered into.</span></span>

## <a name="syntax"></a><span data-ttu-id="97334-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97334-108">Syntax</span></span>


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a><span data-ttu-id="97334-109">Members</span><span class="sxs-lookup"><span data-stu-id="97334-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="97334-110">**ParentDirectory**</span><span class="sxs-lookup"><span data-stu-id="97334-110">**ParentDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="97334-111">Riferimento file alla directory che indicizza il nome.</span><span class="sxs-lookup"><span data-stu-id="97334-111">A file reference to the directory that indexes to this name.</span></span> <span data-ttu-id="97334-112">Vedere informazioni di [**\_ \_ riferimento sul segmento MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="97334-112">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="97334-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="97334-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="97334-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="97334-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97334-115">**FileNameLength**</span><span class="sxs-lookup"><span data-stu-id="97334-115">**FileNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="97334-116">Lunghezza del nome file, in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="97334-116">The length of the file name, in Unicode characters.</span></span>

</dd> <dt>

<span data-ttu-id="97334-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="97334-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="97334-118">Flag del nome file.</span><span class="sxs-lookup"><span data-stu-id="97334-118">The file name flags.</span></span>

<dl> <dt>

<span data-ttu-id="97334-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**File \_ NOME \_ NTFS** (0x01)</span><span class="sxs-lookup"><span data-stu-id="97334-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE\_NAME\_NTFS** (0x01)</span></span>
</dt> <dt>

<span data-ttu-id="97334-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**File \_ NOME \_ DOS** (0x02)</span><span class="sxs-lookup"><span data-stu-id="97334-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE\_NAME\_DOS** (0x02)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="97334-121">**FileName**</span><span class="sxs-lookup"><span data-stu-id="97334-121">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="97334-122">Primo carattere del nome file.</span><span class="sxs-lookup"><span data-stu-id="97334-122">The first character of the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97334-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="97334-123">Remarks</span></span>

<span data-ttu-id="97334-124">Si noti che non è presente alcun file di intestazione associato per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="97334-124">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="97334-125">Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="97334-125">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="97334-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97334-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97334-127">Tabella file master</span><span class="sxs-lookup"><span data-stu-id="97334-127">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
