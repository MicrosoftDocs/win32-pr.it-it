---
title: Proprietà GlobalVoiceCommandsEnabled
description: Proprietà GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963093"
---
# <a name="globalvoicecommandsenabled-property"></a><span data-ttu-id="f7b17-103">Proprietà GlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="f7b17-103">GlobalVoiceCommandsEnabled Property</span></span>

<span data-ttu-id="f7b17-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f7b17-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f7b17-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f7b17-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f7b17-106">Restituisce o imposta un valore che indica se la voce è abilitata per i comandi globali dell'agente.</span><span class="sxs-lookup"><span data-stu-id="f7b17-106">Returns or sets whether voice is enabled for Agent's global commands.</span></span>

</dd> <dt>

<span data-ttu-id="f7b17-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="f7b17-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f7b17-108">*agente. ***Caratteri ("*** CharacterID \* \* *"). Commands. GlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f7b17-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Commands.GlobalVoiceCommandsEnabled**</span></span>

<span data-ttu-id="f7b17-109">\[ = *Boolean*\]</span><span class="sxs-lookup"><span data-stu-id="f7b17-109">\[ = *boolean*\]</span></span>



| <span data-ttu-id="f7b17-110">Parte</span><span class="sxs-lookup"><span data-stu-id="f7b17-110">Part</span></span>      | <span data-ttu-id="f7b17-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7b17-111">Description</span></span>                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b17-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="f7b17-112">*boolean*</span></span> | <span data-ttu-id="f7b17-113">Espressione booleana che indica se i parametri vocali per i comandi globali dell'agente sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="f7b17-113">A Boolean expression that indicates whether voice parameters for Agent's global commands are enabled.</span></span> <span data-ttu-id="f7b17-114">**True** (impostazione predefinita) i parametri vocali sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="f7b17-114">**True** (Default) Voice parameters are enabled.</span></span> <br/> <span data-ttu-id="f7b17-115">**False** I parametri vocali sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="f7b17-115">**False** Voice parameters are disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7b17-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7b17-116">Remarks</span></span>

<span data-ttu-id="f7b17-117">Microsoft Agent aggiunge automaticamente i parametri vocali (grammatica) per l'apertura e la chiusura della finestra dei comandi vocali e per visualizzare e nascondere il carattere.</span><span class="sxs-lookup"><span data-stu-id="f7b17-117">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="f7b17-118">Se si imposta **GlobalVoiceCommandsEnabled** su **false**, Agent Disabilita tutti i parametri vocali per questi comandi, nonché i parametri vocali per la [**didascalia**](caption-property.md) degli oggetti [**comandi**](/windows/desktop/lwef/the-commands-collection-object) di altri client.</span><span class="sxs-lookup"><span data-stu-id="f7b17-118">If you set **GlobalVoiceCommandsEnabled** to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Commands**](/windows/desktop/lwef/the-commands-collection-object) objects.</span></span> <span data-ttu-id="f7b17-119">In questo modo è possibile eliminarli dalla grammatica attiva corrente del client.</span><span class="sxs-lookup"><span data-stu-id="f7b17-119">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="f7b17-120">Tuttavia, poiché questo potrebbe bloccare l'accesso vocale ad altri client, reimpostare questa proprietà su **true** dopo l'elaborazione dell'input vocale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f7b17-120">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="f7b17-121">La disabilitazione della proprietà non influisce sul menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="f7b17-121">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="f7b17-122">Verranno comunque visualizzati i comandi globali aggiunti dal server.</span><span class="sxs-lookup"><span data-stu-id="f7b17-122">The global commands added by the server will still appear.</span></span> <span data-ttu-id="f7b17-123">Non è possibile rimuoverli dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="f7b17-123">You cannot remove them from the pop-up menu.</span></span>

 

