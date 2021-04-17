---
description: Se questo criterio di sistema per computer è impostato su 1, nessun pacchetto nel sistema ottiene la funzionalità del componente condiviso abilitata dall'attributo msidbComponentAttributesShared nella tabella dei componenti.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527037"
---
# <a name="disablesharedcomponent"></a><span data-ttu-id="b6f66-103">DisableSharedComponent</span><span class="sxs-lookup"><span data-stu-id="b6f66-103">DisableSharedComponent</span></span>

<span data-ttu-id="b6f66-104">Se questo [criterio di sistema](system-policy.md) per computer è impostato su 1, nessun pacchetto nel sistema ottiene la funzionalità del componente condiviso abilitata dall'attributo **msidbComponentAttributesShared** nella [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b6f66-104">If this per-machine [system policy](system-policy.md) is set to 1, no package on the system gets the shared component functionality enabled by the **msidbComponentAttributesShared** attribute in the [Component table](component-table.md).</span></span> <span data-ttu-id="b6f66-105">Il valore predefinito è 0, che consente la funzionalità del componente condiviso per i componenti contrassegnati con **msidbComponentAttributesShared** in tutti i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="b6f66-105">The default value is 0, which enables the shared component functionality for components marked with **msidbComponentAttributesShared** in all packages.</span></span>

<span data-ttu-id="b6f66-106">**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="b6f66-106">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="b6f66-107">Questa funzione è disponibile a partire da Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="b6f66-107">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="b6f66-108">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b6f66-108">Registry Key</span></span>

<span data-ttu-id="b6f66-109">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="b6f66-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="b6f66-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b6f66-110">Data Type</span></span>

<span data-ttu-id="b6f66-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b6f66-111">**REG\_DWORD**</span></span>

 

 



