---
description: Se il criterio di sistema per utente è impostato su &\# 0034; 1&\# 0034;, il programma di installazione cerca i file di trasformazione nella radice di tutte le origini di rete nell'elenco di origine per il prodotto. Per impostazione predefinita, le trasformazioni vengono archiviate nella cartella Application Data del profilo di un utente.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: Criteri di TransformsAtSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be9c56f2e68a27d904acf98088204dc4012b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128107"
---
# <a name="transformsatsource-policy"></a><span data-ttu-id="51379-104">Criteri di TransformsAtSource</span><span class="sxs-lookup"><span data-stu-id="51379-104">TransformsAtSource Policy</span></span>

<span data-ttu-id="51379-105">Se il [criterio di sistema](system-policy.md) per utente è impostato su "1"; il programma di installazione cerca i file di trasformazione nella radice di qualsiasi origine di rete nell'elenco di origine per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="51379-105">If this per-user [system policy](system-policy.md) is set to "1"; the installer searches for transform files in the root of any network sources in the source list for the product.</span></span> <span data-ttu-id="51379-106">Per impostazione predefinita, le trasformazioni vengono archiviate nella cartella Application Data del profilo di un utente.</span><span class="sxs-lookup"><span data-stu-id="51379-106">By default, transforms are stored in the Application Data folder of a user's profile.</span></span>

<span data-ttu-id="51379-107">Windows Installer interpreta il criterio TransformsAtSource in modo che corrisponda al [criterio TRANSFORMSSECURE](transformssecure-policy.md).</span><span class="sxs-lookup"><span data-stu-id="51379-107">Windows Installer interprets the TransformsAtSource policy to be the same as the [TransformsSecure policy](transformssecure-policy.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="51379-108">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="51379-108">Registry Key</span></span>

<span data-ttu-id="51379-109">**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="51379-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="51379-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="51379-110">Data Type</span></span>

<span data-ttu-id="51379-111">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="51379-111">**REG\_SZ**</span></span>

 

 



