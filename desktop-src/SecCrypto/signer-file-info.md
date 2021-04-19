---
description: Specifica un file da firmare.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Struttura SIGNER_FILE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317693"
---
# <a name="signer_file_info-structure"></a><span data-ttu-id="edc9b-103">Struttura di \_ informazioni sul file del firmatario \_</span><span class="sxs-lookup"><span data-stu-id="edc9b-103">SIGNER\_FILE\_INFO structure</span></span>

<span data-ttu-id="edc9b-104">La struttura di **\_ \_ informazioni sul file del firmatario** specifica un file da firmare.</span><span class="sxs-lookup"><span data-stu-id="edc9b-104">The **SIGNER\_FILE\_INFO** structure specifies a file to sign.</span></span>

> [!Note]  
> <span data-ttu-id="edc9b-105">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="edc9b-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="edc9b-106">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="edc9b-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="edc9b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edc9b-107">Syntax</span></span>


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a><span data-ttu-id="edc9b-108">Members</span><span class="sxs-lookup"><span data-stu-id="edc9b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="edc9b-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="edc9b-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="edc9b-110">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="edc9b-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="edc9b-111">**pwszFileName**</span><span class="sxs-lookup"><span data-stu-id="edc9b-111">**pwszFileName**</span></span>
</dt> <dd>

<span data-ttu-id="edc9b-112">Puntatore a una stringa con terminazione null che contiene il nome del file da firmare.</span><span class="sxs-lookup"><span data-stu-id="edc9b-112">A pointer to a null-terminated string that contains the name of the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="edc9b-113">**hFile**</span><span class="sxs-lookup"><span data-stu-id="edc9b-113">**hFile**</span></span>
</dt> <dd>

<span data-ttu-id="edc9b-114">Handle aperto per il file specificato dal membro **pwszFileName** .</span><span class="sxs-lookup"><span data-stu-id="edc9b-114">An open handle to the file specified by the **pwszFileName** member.</span></span> <span data-ttu-id="edc9b-115">Se questo membro contiene un handle valido, questo handle viene utilizzato per accedere al file.</span><span class="sxs-lookup"><span data-stu-id="edc9b-115">If this member contains a valid handle, this handle is used to access the file.</span></span> <span data-ttu-id="edc9b-116">Questo membro può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="edc9b-116">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="edc9b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edc9b-117">Requirements</span></span>



| <span data-ttu-id="edc9b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="edc9b-118">Requirement</span></span> | <span data-ttu-id="edc9b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="edc9b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="edc9b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edc9b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="edc9b-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="edc9b-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="edc9b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edc9b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="edc9b-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="edc9b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="edc9b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edc9b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc9b-125">**informazioni sul soggetto del FIRMATARIo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="edc9b-125">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 




