---
title: Proprietà DefaultCommand
description: Proprietà DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046669"
---
# <a name="defaultcommand-property"></a><span data-ttu-id="2f971-103">Proprietà DefaultCommand</span><span class="sxs-lookup"><span data-stu-id="2f971-103">DefaultCommand Property</span></span>

<span data-ttu-id="2f971-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2f971-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2f971-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2f971-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2f971-106">Restituisce o imposta il comando predefinito dell'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2f971-106">Returns or sets the default command of the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span>

</dd> <dt>

<span data-ttu-id="2f971-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="2f971-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2f971-108">*Agent. \* \* \* caratteri* \*  **("***CharacterID***"). Stringa Commands. DefaultCommand** \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="2f971-108">*agent.\*\*\*Characters*\* **("***CharacterID***").Commands.DefaultCommand** \[ = *string*\]</span></span>



| <span data-ttu-id="2f971-109">Parte</span><span class="sxs-lookup"><span data-stu-id="2f971-109">Part</span></span>     | <span data-ttu-id="2f971-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f971-110">Description</span></span>                                                                         |
|----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2f971-111">*string*</span><span class="sxs-lookup"><span data-stu-id="2f971-111">*string*</span></span> | <span data-ttu-id="2f971-112">Valore stringa che identifica il nome (ID) del [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="2f971-112">A string value identifying the name (ID) of the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f971-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f971-113">Remarks</span></span>

<span data-ttu-id="2f971-114">Questa proprietà consente di impostare un [**comando**](/windows/desktop/lwef/the-command-object) nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) come comando predefinito, eseguendone il rendering in grassetto.</span><span class="sxs-lookup"><span data-stu-id="2f971-114">This property enables you to set a [**Command**](/windows/desktop/lwef/the-command-object) in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection as the default command, rendering it bold.</span></span> <span data-ttu-id="2f971-115">Questa operazione non modifica effettivamente la gestione dei comandi o gli eventi di doppio clic.</span><span class="sxs-lookup"><span data-stu-id="2f971-115">This does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="2f971-116">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="2f971-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 