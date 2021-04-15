---
description: Se questo criterio di sistema per computer è impostato su un valore maggiore di 0, Windows Installer Salva le versioni precedenti dei file in una cache quando viene applicata una patch a un'applicazione.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485261"
---
# <a name="maxpatchcachesize"></a><span data-ttu-id="bf1c5-103">MaxPatchCacheSize</span><span class="sxs-lookup"><span data-stu-id="bf1c5-103">MaxPatchCacheSize</span></span>

<span data-ttu-id="bf1c5-104">Se questo [criterio di sistema](system-policy.md) per computer è impostato su un valore maggiore di 0, Windows Installer Salva le versioni precedenti dei file in una cache quando viene applicata una patch a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-104">If this per-machine [system policy](system-policy.md) is set to a value greater than 0, Windows Installer saves older versions of files in a cache when a patch is applied to an application.</span></span> <span data-ttu-id="bf1c5-105">La memorizzazione nella cache può migliorare le prestazioni delle installazioni future che altrimenti dovranno ottenere i vecchi file da un'origine applicazione originale.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-105">Caching can increase the performance of future installations that otherwise need to obtain the old files from a original application source.</span></span>

<span data-ttu-id="bf1c5-106">Il valore del criterio MaxPatchCacheSize è la percentuale massima di spazio su disco che il programma di installazione può utilizzare per la cache dei file obsoleti.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-106">The value of the MaxPatchCacheSize policy is the maximum percentage of disk space that the installer can use for the cache of old files.</span></span> <span data-ttu-id="bf1c5-107">Ad esempio, un valore pari a 20 indica che non viene utilizzato più del 20%.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-107">For example, a value of 20 specifies no more than 20% be used.</span></span> <span data-ttu-id="bf1c5-108">Se la dimensione totale della cache raggiunge la percentuale di spazio su disco specificata, nessun file aggiuntivo viene salvato nella cache.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-108">If the total size of the cache reaches the specified percentage of disk space, no additional files are saved to the cache.</span></span> <span data-ttu-id="bf1c5-109">Il criterio non influisce sui file che sono già stati salvati.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-109">The policy does not affect files that have already been saved.</span></span>

<span data-ttu-id="bf1c5-110">Se il valore del criterio MaxPatchCacheSize è impostato su 0, non viene salvato alcun file aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-110">If the value of the MaxPatchCacheSize policy is set to 0, no additional files are saved.</span></span>

<span data-ttu-id="bf1c5-111">Se il criterio MaxPatchCacheSize non è impostato, il valore predefinito è 10 e un massimo del 10% dello spazio su disco può essere utilizzato per salvare i file obsoleti.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-111">If the MaxPatchCacheSize policy is not set, the default value is 10 and a maximum of 10% of the disk space can be used to save old files.</span></span>

## <a name="registry-key"></a><span data-ttu-id="bf1c5-112">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="bf1c5-112">Registry Key</span></span>

<span data-ttu-id="bf1c5-113">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="bf1c5-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="bf1c5-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bf1c5-114">Data Type</span></span>

<span data-ttu-id="bf1c5-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bf1c5-115">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf1c5-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf1c5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf1c5-117">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="bf1c5-117">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



