---
description: Gestione dello schema di risparmio energia
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Gestione dello schema di risparmio energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312042"
---
# <a name="power-scheme-management"></a><span data-ttu-id="fa91e-103">Gestione dello schema di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="fa91e-103">Power Scheme Management</span></span>

<span data-ttu-id="fa91e-104">Ogni combinazione di energia viene identificata in modo univoco da un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="fa91e-104">Each power scheme is uniquely identified by a **GUID**.</span></span> <span data-ttu-id="fa91e-105">Per enumerare tutte le combinazioni per il risparmio di energia disponibili, usare la funzione [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) .</span><span class="sxs-lookup"><span data-stu-id="fa91e-105">To enumerate all available power schemes, use the [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) function.</span></span> <span data-ttu-id="fa91e-106">**PowerEnumerate** può essere usato anche per recuperare tutte le impostazioni di risparmio energia per uno schema specificato.</span><span class="sxs-lookup"><span data-stu-id="fa91e-106">**PowerEnumerate** can also be used to retrieve all of the power settings for a specified scheme.</span></span>

<span data-ttu-id="fa91e-107">Lo schema di risparmio energia attualmente in uso nel sistema è denominato schema di risparmio energia attivo o piano.</span><span class="sxs-lookup"><span data-stu-id="fa91e-107">The power scheme that is currently in use on the system is called the active power scheme or plan.</span></span> <span data-ttu-id="fa91e-108">Per recuperare il **GUID** del piano attivo, chiamare la funzione [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="fa91e-108">To retrieve the **GUID** of the active plan, call the [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) function.</span></span> <span data-ttu-id="fa91e-109">Per modificare la combinazione per il risparmio di energia attiva, chiamare la funzione [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="fa91e-109">To change the active power plan, call the [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) function.</span></span>

<span data-ttu-id="fa91e-110">Per creare uno schema di risparmio energia, è necessario innanzitutto duplicare uno schema esistente usando la funzione [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) , specificando il **GUID** dello schema su cui si desidera basare il nuovo schema.</span><span class="sxs-lookup"><span data-stu-id="fa91e-110">To create a power scheme, you need to first duplicate an existing scheme by using the [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) function, specifying the **GUID** of the scheme you wish to base your new scheme upon.</span></span> <span data-ttu-id="fa91e-111">È necessario copiare uno degli schemi predefiniti e modificare le impostazioni di risparmio energia in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="fa91e-111">You should copy one of the built-in schemes and modify the power settings to your needs.</span></span> <span data-ttu-id="fa91e-112">Si noti che la creazione di una combinazione per il risparmio di energia non aggiorna automaticamente il risparmio di energia attivo.</span><span class="sxs-lookup"><span data-stu-id="fa91e-112">Note that creating a power plan does not automatically update the active power plan.</span></span> <span data-ttu-id="fa91e-113">È sempre necessario chiamare [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) per aggiornare la combinazione per il risparmio di energia attiva.</span><span class="sxs-lookup"><span data-stu-id="fa91e-113">You must always call [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) to update the active power plan.</span></span> <span data-ttu-id="fa91e-114">Le combinazioni per il risparmio di energia esistenti possono essere modificate e quindi applicate nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="fa91e-114">Existing power plans can be modified and then applied in the same manner.</span></span>

<span data-ttu-id="fa91e-115">Per rimuovere una combinazione per il risparmio di energia, chiamare la funzione [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) .</span><span class="sxs-lookup"><span data-stu-id="fa91e-115">To remove a power plan, call the [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) function.</span></span>

> [!Note]  
> <span data-ttu-id="fa91e-116">Per recuperare informazioni aggiuntive sullo stato di alimentazione del sistema, chiamare la funzione [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) .</span><span class="sxs-lookup"><span data-stu-id="fa91e-116">To retrieve additional information about the system power state, call the [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fa91e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa91e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa91e-118">Combinazioni per il risparmio di energia</span><span class="sxs-lookup"><span data-stu-id="fa91e-118">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 



