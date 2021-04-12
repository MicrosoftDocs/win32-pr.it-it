---
title: Tipo semplice sessionStateChangeType
description: Definisce i valori per il tipo di Terminal Server modifica dello stato della sessione che è possibile usare per avviare un'attività.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Utilità di pianificazione di tipo semplice sessionStateChangeType
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478377"
---
# <a name="sessionstatechangetype-simple-type"></a><span data-ttu-id="dec15-104">Tipo semplice sessionStateChangeType</span><span class="sxs-lookup"><span data-stu-id="dec15-104">sessionStateChangeType Simple Type</span></span>

<span data-ttu-id="dec15-105">Definisce i valori per il tipo di Terminal Server modifica dello stato della sessione che è possibile usare per avviare un'attività.</span><span class="sxs-lookup"><span data-stu-id="dec15-105">Defines values for the kind of Terminal Server session state change you can use to trigger a task to start.</span></span>

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="dec15-106">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="dec15-106">Enumeration values</span></span>

<span data-ttu-id="dec15-107">Il tipo semplice **sessionStateChangeType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dec15-107">The **sessionStateChangeType** simple type defines the following values.</span></span>



| <span data-ttu-id="dec15-108">Valore</span><span class="sxs-lookup"><span data-stu-id="dec15-108">Value</span></span>             | <span data-ttu-id="dec15-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dec15-109">Description</span></span>                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec15-110">ConsoleConnect</span><span class="sxs-lookup"><span data-stu-id="dec15-110">ConsoleConnect</span></span>    | <span data-ttu-id="dec15-111">Modifica dello stato di connessione della console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="dec15-111">Terminal Server console connection state change.</span></span> <span data-ttu-id="dec15-112">Ad esempio, quando si esegue la connessione a una sessione utente nel computer locale cambiando gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="dec15-112">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                            |
| <span data-ttu-id="dec15-113">ConsoleDisconnect</span><span class="sxs-lookup"><span data-stu-id="dec15-113">ConsoleDisconnect</span></span> | <span data-ttu-id="dec15-114">Modifica dello stato di disconnessione della console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="dec15-114">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="dec15-115">Ad esempio, quando si esegue la disconnessione a una sessione utente nel computer locale cambiando gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="dec15-115">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span> <br/>                      |
| <span data-ttu-id="dec15-116">RemoteConnect</span><span class="sxs-lookup"><span data-stu-id="dec15-116">RemoteConnect</span></span>     | <span data-ttu-id="dec15-117">Terminal Server modifica dello stato della connessione remota.</span><span class="sxs-lookup"><span data-stu-id="dec15-117">Terminal Server remote connection state change.</span></span> <span data-ttu-id="dec15-118">Ad esempio, quando un utente si connette a una sessione utente utilizzando il programma Connessione Desktop remoto da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="dec15-118">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span> <br/>            |
| <span data-ttu-id="dec15-119">RemoteDisconnect</span><span class="sxs-lookup"><span data-stu-id="dec15-119">RemoteDisconnect</span></span>  | <span data-ttu-id="dec15-120">Terminal Server modifica dello stato di disconnessione remota.</span><span class="sxs-lookup"><span data-stu-id="dec15-120">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="dec15-121">Ad esempio, quando un utente si disconnette da una sessione utente durante l'utilizzo del programma Connessione Desktop remoto da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="dec15-121">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span> <br/> |
| <span data-ttu-id="dec15-122">SessionLock</span><span class="sxs-lookup"><span data-stu-id="dec15-122">SessionLock</span></span>       | <span data-ttu-id="dec15-123">Modifica dello stato di blocco della sessione Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="dec15-123">Terminal Server session locked state change.</span></span> <span data-ttu-id="dec15-124">Ad esempio, questa modifica di stato comporta l'esecuzione dell'attività quando il computer è bloccato.</span><span class="sxs-lookup"><span data-stu-id="dec15-124">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                       |
| <span data-ttu-id="dec15-125">SessionUnlock</span><span class="sxs-lookup"><span data-stu-id="dec15-125">SessionUnlock</span></span>     | <span data-ttu-id="dec15-126">Modifica dello stato di Terminal Server sessione sbloccata.</span><span class="sxs-lookup"><span data-stu-id="dec15-126">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="dec15-127">Ad esempio, questa modifica di stato comporta l'esecuzione dell'attività quando il computer è sbloccato.</span><span class="sxs-lookup"><span data-stu-id="dec15-127">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                    |



## <a name="requirements"></a><span data-ttu-id="dec15-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dec15-128">Requirements</span></span>



| <span data-ttu-id="dec15-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec15-129">Requirement</span></span> | <span data-ttu-id="dec15-130">Valore</span><span class="sxs-lookup"><span data-stu-id="dec15-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dec15-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dec15-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dec15-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dec15-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dec15-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dec15-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dec15-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dec15-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





