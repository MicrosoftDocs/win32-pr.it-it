---
description: Questo criterio di sistema per computer può essere usato per specificare che il Windows Installer passare tutte le proprietà pubbliche al lato server durante un'installazione gestita usando privilegi elevati.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130686"
---
# <a name="enableusercontrol"></a><span data-ttu-id="24edb-103">EnableUserControl</span><span class="sxs-lookup"><span data-stu-id="24edb-103">EnableUserControl</span></span>

<span data-ttu-id="24edb-104">Nel caso di un'installazione gestita, l'autore del pacchetto potrebbe dover limitare le proprietà pubbliche che vengono passate al lato server e possono essere modificate da un utente che non è un amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="24edb-104">In the case of a managed installation, the package author may need to limit which public properties are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="24edb-105">Alcune restrizioni sono in genere necessarie per mantenere un ambiente protetto quando l'installazione richiede che il programma di installazione utilizzi privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="24edb-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span>

<span data-ttu-id="24edb-106">Se il [criterio di sistema](system-policy.md) per computer è impostato su "1", il programma di installazione può passare tutte le [proprietà pubbliche](public-properties.md) al lato server durante un'installazione gestita utilizzando privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="24edb-106">If this per-machine [system policy](system-policy.md) is set to "1", then the installer can pass all [public properties](public-properties.md) to the server side during a managed installation using elevated privileges.</span></span> <span data-ttu-id="24edb-107">L'impostazione di questo criterio ha lo stesso effetto dell'impostazione della proprietà **EnableUserControl** .</span><span class="sxs-lookup"><span data-stu-id="24edb-107">Setting this policy has the same effect as setting the **EnableUserControl** property.</span></span> <span data-ttu-id="24edb-108">L'impostazione di questo criterio consente di passare tutte le proprietà pubbliche al servizio e di modificarle dagli utenti non amministrativi.</span><span class="sxs-lookup"><span data-stu-id="24edb-108">Setting this policy allows all public properties to be passed to the service and to be changeable by nonadministrative users.</span></span> <span data-ttu-id="24edb-109">Per impostazione predefinita, questo criterio non è abilitato. solo le proprietà pubbliche con restrizioni vengono passate al lato server e possono essere modificate da un utente non amministratore.</span><span class="sxs-lookup"><span data-stu-id="24edb-109">By default, this policy is not enabled; only restricted public properties are passed to the server side and changeable by a nonadministrative user.</span></span> <span data-ttu-id="24edb-110">Tutte le altre proprietà pubbliche vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="24edb-110">All other public properties are ignored.</span></span>

<span data-ttu-id="24edb-111">Se il sistema operativo è Windows 2000, l'utente non è un amministratore di sistema e l'applicazione o il prodotto viene installato con privilegi elevati, un utente che non è un amministratore di sistema può solo eseguire l'override di un elenco approvato di proprietà pubbliche limitate.</span><span class="sxs-lookup"><span data-stu-id="24edb-111">If the operating system is Windows 2000, the user is not a system administrator, and the application or product is being installed with elevated privileges, then a user that is not a system administrator can only override an approved list of restricted public properties.</span></span> <span data-ttu-id="24edb-112">Per ulteriori informazioni, vedere [proprietà pubbliche limitate](restricted-public-properties.md).</span><span class="sxs-lookup"><span data-stu-id="24edb-112">For more information see [Restricted Public Properties](restricted-public-properties.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="24edb-113">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="24edb-113">Registry Key</span></span>

<span data-ttu-id="24edb-114">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="24edb-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="24edb-115">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="24edb-115">Data Type</span></span>

<span data-ttu-id="24edb-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="24edb-116">**REG\_DWORD**</span></span>

 

 



