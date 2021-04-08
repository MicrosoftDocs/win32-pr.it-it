---
description: PROPERTYKEYs e GUID nei dispositivi portatili Windows
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs e GUID nei dispositivi portatili Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883150"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a><span data-ttu-id="d7a8b-103">PROPERTYKEYs e GUID nei dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="d7a8b-103">PROPERTYKEYs and GUIDs in Windows Portable Devices</span></span>

<span data-ttu-id="d7a8b-104">Una proprietà o un comando è identificato da una struttura PROPERTYKEY.</span><span class="sxs-lookup"><span data-stu-id="d7a8b-104">A property or command is identified by a PROPERTYKEY structure.</span></span> <span data-ttu-id="d7a8b-105">Una struttura PROPERTYKEY è costituita da due parti: un GUID (il membro fmtid) e un valore DWORD (il membro PID).</span><span class="sxs-lookup"><span data-stu-id="d7a8b-105">A PROPERTYKEY structure is made up of two parts: a GUID (the fmtid member) and a DWORD (the pid member).</span></span> <span data-ttu-id="d7a8b-106">La parte GUID viene utilizzata per indicare la categoria a cui appartiene la proprietà o il comando (ovvero, le proprietà correlate appartengono alla stessa categoria e i comandi correlati appartengono alla stessa categoria; pertanto avranno lo stesso fmtid).</span><span class="sxs-lookup"><span data-stu-id="d7a8b-106">The GUID part is used to indicate the category the property or command belongs to (that is, related properties belong to the same category and related commands belong to the same category; therefore they will have the same fmtid).</span></span> <span data-ttu-id="d7a8b-107">La parte DWORD indica l'ID della proprietà o del comando e viene utilizzata per distinguere le singole proprietà o comandi all'interno di una proprietà o di una categoria di comandi, ovvero i valori PID per le proprietà o i comandi nella stessa categoria saranno diversi.</span><span class="sxs-lookup"><span data-stu-id="d7a8b-107">The DWORD part indicates the property or command ID, and is used to distinguish the individual properties or commands within a property or command category (that is, the pid values for properties or commands in the same category will be different).</span></span>

<span data-ttu-id="d7a8b-108">La sezione di riferimento di questo documento descrive tutti i valori PROPERTYKEY definiti da WPD; questi valori corrispondono a comandi, proprietà e risorse.</span><span class="sxs-lookup"><span data-stu-id="d7a8b-108">The reference section of this document describes all the PROPERTYKEY values defined by WPD; these values correspond to commands, properties, and resources.</span></span> <span data-ttu-id="d7a8b-109">Se si crea un valore PROPERTYKEY personalizzato, è necessario definire una nuova categoria **GUID** ; Non riutilizzare i valori **GUID** WPD o rischiare conflitti con PROPERTYKEYs esistenti e futuri specificati da WPD.</span><span class="sxs-lookup"><span data-stu-id="d7a8b-109">If you create a custom PROPERTYKEY value, you should define a new **GUID** category; do not reuse the WPD **GUID** values or you risk conflicting with existing and future WPD-specified PROPERTYKEYs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7a8b-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7a8b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7a8b-111">**Panoramica dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="d7a8b-111">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="d7a8b-112">**Comandi**</span><span class="sxs-lookup"><span data-stu-id="d7a8b-112">**Commands**</span></span>](commands.md)
</dt> <dt>

[<span data-ttu-id="d7a8b-113">**GUID formato oggetto**</span><span class="sxs-lookup"><span data-stu-id="d7a8b-113">**Object Format GUIDs**</span></span>](object-format-guids.md)
</dt> <dt>

[<span data-ttu-id="d7a8b-114">**Proprietà e attributi**</span><span class="sxs-lookup"><span data-stu-id="d7a8b-114">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7a8b-115">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="d7a8b-115">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



