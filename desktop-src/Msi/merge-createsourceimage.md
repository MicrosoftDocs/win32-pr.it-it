---
description: Il metodo CreateSourceImage dell'oggetto merge consente al client di estrarre i file da un modulo in un'immagine di origine su disco dopo un'operazione di merge, tenendo conto delle modifiche apportate al modulo che potrebbero essere state apportate durante la configurazione del modulo.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Metodo merge. CreateSourceImage (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327807"
---
# <a name="mergecreatesourceimage-method"></a><span data-ttu-id="07e81-103">Merge. CreateSourceImage, metodo</span><span class="sxs-lookup"><span data-stu-id="07e81-103">Merge.CreateSourceImage method</span></span>

<span data-ttu-id="07e81-104">Il metodo **CreateSourceImage** dell'oggetto [**merge**](merge-object.md) consente al client di estrarre i file da un modulo in un'immagine di origine su disco dopo un'operazione di merge, tenendo conto delle modifiche apportate al modulo che potrebbero essere state apportate durante la configurazione del modulo.</span><span class="sxs-lookup"><span data-stu-id="07e81-104">The **CreateSourceImage** method of the [**Merge**](merge-object.md) object allows the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration.</span></span> <span data-ttu-id="07e81-105">L'elenco di file da estrarre viene ricavato dalla tabella file del modulo durante il processo di merge.</span><span class="sxs-lookup"><span data-stu-id="07e81-105">The list of files to be extracted is taken from the file table of the module during the merge process.</span></span> <span data-ttu-id="07e81-106">L'elenco dei file è costituito da tutti i file copiati correttamente dalla tabella file del modulo al database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="07e81-106">The list of files consists of every file successfully copied from the file table of the module to the target database.</span></span> <span data-ttu-id="07e81-107">Le voci della tabella di file non copiate a causa di conflitti di chiave primaria con le righe esistenti nel database non fanno parte di questo elenco.</span><span class="sxs-lookup"><span data-stu-id="07e81-107">File table entries that were not copied due to primary key conflicts with existing rows in the database are not a part of this list.</span></span> <span data-ttu-id="07e81-108">Al momento della creazione dell'immagine, la directory per ognuno di questi file deriva dal database aperto (post-merge).</span><span class="sxs-lookup"><span data-stu-id="07e81-108">At image creation time, the directory for each of these files comes from the open (post-merge) database.</span></span> <span data-ttu-id="07e81-109">Il percorso specificato nel parametro *path* è la radice dell'immagine di origine per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="07e81-109">The path specified in the *Path* parameter is the root of the source image for the install.</span></span> <span data-ttu-id="07e81-110">*fLongFileNames* determina se i nomi di file lunghi vengono usati sia per i segmenti di percorso che per i nomi di file finali.</span><span class="sxs-lookup"><span data-stu-id="07e81-110">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span> <span data-ttu-id="07e81-111">La funzione ha esito negativo se non è aperto alcun database, non è aperto alcun modulo oppure non è stata eseguita alcuna operazione di merge.</span><span class="sxs-lookup"><span data-stu-id="07e81-111">The function fails if no database is open, no module is open, or no merge has been performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e81-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07e81-112">Syntax</span></span>


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="07e81-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="07e81-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07e81-114">*Percorso*</span><span class="sxs-lookup"><span data-stu-id="07e81-114">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="07e81-115">Percorso della radice dell'immagine di origine per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="07e81-115">The path of the root of the source image for the install.</span></span>

</dd> <dt>

<span data-ttu-id="07e81-116">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="07e81-116">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="07e81-117">*fLongFileNames* determina se i nomi di file lunghi vengono usati sia per i segmenti di percorso che per i nomi di file finali.</span><span class="sxs-lookup"><span data-stu-id="07e81-117">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="07e81-118">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="07e81-118">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="07e81-119">Si tratta di un elenco di percorsi completi per i file estratti correttamente.</span><span class="sxs-lookup"><span data-stu-id="07e81-119">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07e81-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07e81-120">Return value</span></span>

<span data-ttu-id="07e81-121">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="07e81-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07e81-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="07e81-122">Remarks</span></span>

<span data-ttu-id="07e81-123">Tutti i file nella directory di destinazione con lo stesso nome verranno sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="07e81-123">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="07e81-124">Il percorso viene creato se non esiste già.</span><span class="sxs-lookup"><span data-stu-id="07e81-124">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="07e81-125">C++</span><span class="sxs-lookup"><span data-stu-id="07e81-125">C++</span></span>

<span data-ttu-id="07e81-126">Vedere funzione [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) .</span><span class="sxs-lookup"><span data-stu-id="07e81-126">See [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="07e81-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07e81-127">Requirements</span></span>



| <span data-ttu-id="07e81-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="07e81-128">Requirement</span></span> | <span data-ttu-id="07e81-129">Valore</span><span class="sxs-lookup"><span data-stu-id="07e81-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07e81-130">Versione</span><span class="sxs-lookup"><span data-stu-id="07e81-130">Version</span></span><br/> | <span data-ttu-id="07e81-131">Mergemod.dll 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="07e81-131">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="07e81-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07e81-132">Header</span></span><br/>  | <dl> <span data-ttu-id="07e81-133"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="07e81-133"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="07e81-134">DLL</span><span class="sxs-lookup"><span data-stu-id="07e81-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="07e81-135"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07e81-135"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




