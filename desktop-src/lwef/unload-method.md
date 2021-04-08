---
title: Metodo Unload
description: Metodo Unload
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725914"
---
# <a name="unload-method"></a><span data-ttu-id="b84d0-103">Metodo Unload</span><span class="sxs-lookup"><span data-stu-id="b84d0-103">Unload Method</span></span>

<span data-ttu-id="b84d0-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b84d0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b84d0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b84d0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b84d0-106">Scarica i dati di tipo carattere per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="b84d0-106">Unloads the character data for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="b84d0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="b84d0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b84d0-108">*agente ***. Caratteri. Unload "*** CharacterID \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="b84d0-108">*agent ***.Characters.Unload "*** CharacterID\*\*\*"*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b84d0-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b84d0-109">Remarks</span></span>

<span data-ttu-id="b84d0-110">Utilizzare questo metodo quando non è più necessario un carattere, per liberare memoria utilizzata per archiviare le informazioni sul carattere.</span><span class="sxs-lookup"><span data-stu-id="b84d0-110">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="b84d0-111">Se si accede di nuovo al carattere, utilizzare il metodo [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="b84d0-111">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

<span data-ttu-id="b84d0-112">Questo metodo non restituisce un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="b84d0-112">This method does not return a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 