---
title: Proprietà IdleOn
description: Proprietà IdleOn
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328196"
---
# <a name="idleon-property"></a><span data-ttu-id="a7e76-103">Proprietà IdleOn</span><span class="sxs-lookup"><span data-stu-id="a7e76-103">IdleOn Property</span></span>

<span data-ttu-id="a7e76-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a7e76-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a7e76-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a7e76-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a7e76-106">Restituisce o imposta un valore booleano che determina se il server gestisce le animazioni di stato **minimo** del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="a7e76-106">Returns or sets a Boolean value that determines whether the server manages the specified character's **Idling** state animations.</span></span>

</dd> <dt>

<span data-ttu-id="a7e76-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a7e76-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a7e76-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). IdleOn*( \*  \[  =  *booleano* )\]</span><span class="sxs-lookup"><span data-stu-id="a7e76-108">*agent ***.Characters ("*** CharacterID\*\*\*").IdleOn*\* \[ = *boolean*\]</span></span>

</dd> </dl> 

| <span data-ttu-id="a7e76-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a7e76-109">Part</span></span>      | <span data-ttu-id="a7e76-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7e76-110">Description</span></span>                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e76-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="a7e76-111">*boolean*</span></span> | <span data-ttu-id="a7e76-112">Espressione booleana che specifica se il server gestisce la modalità di inattività.</span><span class="sxs-lookup"><span data-stu-id="a7e76-112">A Boolean expression specifying whether the server manages idle mode.</span></span> <span data-ttu-id="a7e76-113">**True** (impostazione predefinita) la gestione del server dello stato inattivo è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a7e76-113">**True** (Default) Server handling of the idle state is enabled.</span></span> <br/> <span data-ttu-id="a7e76-114">**False** La gestione del server dello stato inattivo è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a7e76-114">**False** Server handling of the idle state is disabled.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7e76-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7e76-115">Remarks</span></span>

<span data-ttu-id="a7e76-116">Il server imposta automaticamente un timeout dopo l'ultima animazione riprodotta per un carattere.</span><span class="sxs-lookup"><span data-stu-id="a7e76-116">The server automatically sets a time-out after the last animation played for a character.</span></span> <span data-ttu-id="a7e76-117">Quando l'intervallo di questo timer è completo, il server inizia **lo stato di** inattivo per un carattere, eseguendo le animazioni al **minimo** associate a intervalli regolari.</span><span class="sxs-lookup"><span data-stu-id="a7e76-117">When this timer's interval is complete, the server begins the **Idling** state for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="a7e76-118">Se si desidera disabilitare il server **per la riproduzione** automatica delle animazioni di stato di inattivo, impostare la proprietà su **false** e riprodurre un'animazione oppure chiamare il metodo [**Stop**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="a7e76-118">If you want to disable the server from automatically playing the **Idling** state animations, set the property to **False** and play an animation or call the [**Stop**](stop-method.md) method.</span></span> <span data-ttu-id="a7e76-119">L'impostazione di questo valore non influisce sullo stato di animazione corrente del carattere.</span><span class="sxs-lookup"><span data-stu-id="a7e76-119">Setting this value does not affect the current animation state of the character.</span></span>

<span data-ttu-id="a7e76-120">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a7e76-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 





