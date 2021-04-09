---
description: Se il criterio di sistema per computer è impostato su 1, la funzionalità di utilizzo dell'interfaccia utente incorporata è disabilitata nel computer. Il valore predefinito è 0, che consente la funzionalità di gestori dell'interfaccia utente incorporata.
ms.assetid: f69d69a3-3c28-4841-a334-3acb61a06bc2
title: MsiDisableEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f5bfe6abfbb386253631c2858dab6ef36bcf39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968585"
---
# <a name="msidisableembeddedui"></a><span data-ttu-id="a2e8a-104">MsiDisableEmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="a2e8a-104">MsiDisableEmbeddedUI</span></span>

<span data-ttu-id="a2e8a-105">Se il [criterio di sistema](system-policy.md) per computer è impostato su 1, la funzionalità di utilizzo dell'interfaccia utente incorporata è disabilitata nel computer.</span><span class="sxs-lookup"><span data-stu-id="a2e8a-105">If this per-machine [system policy](system-policy.md) is set to 1, the capability to use embedded UI is disabled on the computer.</span></span> <span data-ttu-id="a2e8a-106">Il valore predefinito è 0, che consente la funzionalità di gestori dell'interfaccia utente incorporata.</span><span class="sxs-lookup"><span data-stu-id="a2e8a-106">The default value is 0, which enables the embedded UI handlers capability.</span></span>

<span data-ttu-id="a2e8a-107">Per disabilitare l'interfaccia utente incorporata per un singolo pacchetto, è possibile usare la proprietà [**MSIDISABLEEEUI**](msidisableeeui.md) .</span><span class="sxs-lookup"><span data-stu-id="a2e8a-107">To disable the embedded UI for a single package, you can use the [**MSIDISABLEEEUI**](msidisableeeui.md) property.</span></span>

<span data-ttu-id="a2e8a-108">**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="a2e8a-108">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="a2e8a-109">Questa funzione è disponibile a partire da Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="a2e8a-109">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="a2e8a-110">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="a2e8a-110">Registry Key</span></span>

<span data-ttu-id="a2e8a-111">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="a2e8a-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="a2e8a-112">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a2e8a-112">Data Type</span></span>

<span data-ttu-id="a2e8a-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a2e8a-113">**REG\_DWORD**</span></span>

 

 



