---
title: Proprietà Count
description: Proprietà Count
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872394"
---
# <a name="count-property"></a><span data-ttu-id="5a7de-103">Proprietà Count</span><span class="sxs-lookup"><span data-stu-id="5a7de-103">Count Property</span></span>

<span data-ttu-id="5a7de-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a7de-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5a7de-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5a7de-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5a7de-106">Restituisce un valore Long Integer (proprietà di sola lettura) che specifica il numero di oggetti [**Command**](/windows/desktop/lwef/the-command-object) nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="5a7de-106">Returns a Long integer (read-only property) that specifies the count of [**Command**](/windows/desktop/lwef/the-command-object) objects in the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="5a7de-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="5a7de-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5a7de-108">*agente ***. Caratteri ("*** CharacterID \* \* *"). Commands. Count**</span><span class="sxs-lookup"><span data-stu-id="5a7de-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Count*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a7de-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a7de-109">Remarks</span></span>

<span data-ttu-id="5a7de-110">Il **conteggio** include solo il numero di oggetti [**Command**](/windows/desktop/lwef/the-command-object) definiti nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="5a7de-110">**Count** includes only the number of [**Command**](/windows/desktop/lwef/the-command-object) objects you define in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="5a7de-111">Il server o altre voci client non sono incluse.</span><span class="sxs-lookup"><span data-stu-id="5a7de-111">Server or other client entries are not included.</span></span>

 

 