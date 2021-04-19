---
description: 'I valori del registro di sistema di WFP si trovano nella seguente chiave del registro di sistema: HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valori del registro di sistema WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317621"
---
# <a name="wfp-registry-values"></a><span data-ttu-id="2479b-103">Valori del registro di sistema WFP</span><span class="sxs-lookup"><span data-stu-id="2479b-103">WFP Registry Values</span></span>

<span data-ttu-id="2479b-104">\[I valori del registro di sistema WFP non sono supportati a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="2479b-104">\[WFP registry values are not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="2479b-105">WFP utilizza diversi valori del registro di sistema per le impostazioni di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="2479b-105">WFP uses several registry values for customization settings.</span></span> <span data-ttu-id="2479b-106">I valori del registro di sistema di WFP si trovano nella seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="2479b-106">The WFP registry values are located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

<span data-ttu-id="2479b-107">Di seguito sono riportati i valori del registro di sistema di WFP.</span><span class="sxs-lookup"><span data-stu-id="2479b-107">The following are the WFP registry values.</span></span>

<dl> <dt>

<span data-ttu-id="2479b-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span><span class="sxs-lookup"><span data-stu-id="2479b-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span></span>
</dt> <dd>

<span data-ttu-id="2479b-109">Percorso della cache.</span><span class="sxs-lookup"><span data-stu-id="2479b-109">Location of the cache.</span></span> <span data-ttu-id="2479b-110">Deve trattarsi di un percorso locale.</span><span class="sxs-lookup"><span data-stu-id="2479b-110">This must be a local path.</span></span> <span data-ttu-id="2479b-111">Il valore predefinito è% SystemRoot% \\ system32 \\ dllcache.</span><span class="sxs-lookup"><span data-stu-id="2479b-111">The default value is %systemroot%\\system32\\dllcache.</span></span>

</dd> <dt>

<span data-ttu-id="2479b-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span><span class="sxs-lookup"><span data-stu-id="2479b-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span></span>
</dt> <dd>

<span data-ttu-id="2479b-113">Opzioni di quota.</span><span class="sxs-lookup"><span data-stu-id="2479b-113">Quota options.</span></span> <span data-ttu-id="2479b-114">Il valore del registro di sistema può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2479b-114">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="2479b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2479b-115">Value</span></span>                  | <span data-ttu-id="2479b-116">Significato</span><span class="sxs-lookup"><span data-stu-id="2479b-116">Meaning</span></span>                                                  |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="2479b-117">SFC \_ quota \_ tutti \_ i file</span><span class="sxs-lookup"><span data-stu-id="2479b-117">SFC\_QUOTA\_ALL\_FILES</span></span> | <span data-ttu-id="2479b-118">Le dimensioni della cache DLL sono illimitate.</span><span class="sxs-lookup"><span data-stu-id="2479b-118">Size of the DLL cache is unlimited.</span></span> <span data-ttu-id="2479b-119">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2479b-119">This is the default.</span></span> |
| <span data-ttu-id="2479b-120">Altri valori</span><span class="sxs-lookup"><span data-stu-id="2479b-120">Other values</span></span>           | <span data-ttu-id="2479b-121">Dimensione della cache DLL, in file.</span><span class="sxs-lookup"><span data-stu-id="2479b-121">Size of the DLL cache, in files.</span></span>                         |



 

</dd> <dt>

<span data-ttu-id="2479b-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span><span class="sxs-lookup"><span data-stu-id="2479b-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span></span>
</dt> <dd>

<span data-ttu-id="2479b-123">Opzioni di analisi.</span><span class="sxs-lookup"><span data-stu-id="2479b-123">Scan options.</span></span> <span data-ttu-id="2479b-124">Il valore del registro di sistema può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2479b-124">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="2479b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2479b-125">Value</span></span>             | <span data-ttu-id="2479b-126">Significato</span><span class="sxs-lookup"><span data-stu-id="2479b-126">Meaning</span></span>                                                   |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="2479b-127">Analisi SFC- \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="2479b-127">SFC\_SCAN\_NORMAL</span></span> | <span data-ttu-id="2479b-128">Non eseguire l'analisi dei file protetti all'avvio.</span><span class="sxs-lookup"><span data-stu-id="2479b-128">Do not scan protected files at boot.</span></span> <span data-ttu-id="2479b-129">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2479b-129">This is the default.</span></span> |
| <span data-ttu-id="2479b-130">\_Analisi SFC \_ sempre</span><span class="sxs-lookup"><span data-stu-id="2479b-130">SFC\_SCAN\_ALWAYS</span></span> | <span data-ttu-id="2479b-131">Analizza i file protetti a ogni avvio.</span><span class="sxs-lookup"><span data-stu-id="2479b-131">Scan protected files at every boot.</span></span>                       |
| <span data-ttu-id="2479b-132">\_Analisi SFC \_ una volta</span><span class="sxs-lookup"><span data-stu-id="2479b-132">SFC\_SCAN\_ONCE</span></span>   | <span data-ttu-id="2479b-133">Analizza i file protetti all'avvio successivo.</span><span class="sxs-lookup"><span data-stu-id="2479b-133">Scan protected files at the next boot.</span></span>                    |



 

</dd> </dl>

 

 



