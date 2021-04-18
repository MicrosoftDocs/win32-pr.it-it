---
description: Indica la posizione in cui eseguire la ricerca di un Active Directory archivio certificati.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Enumerazione CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326042"
---
# <a name="capicom_active_directory_search_location-enumeration"></a><span data-ttu-id="87c0b-103">\_Enumerazione del percorso di ricerca di Active \_ directory di \_ CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="87c0b-103">CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION enumeration</span></span>

<span data-ttu-id="87c0b-104">Il tipo di enumerazione del **\_ percorso di ricerca di Active \_ directory \_ \_ di CAPICOM** indica la posizione in cui eseguire la ricerca di un [*archivio certificati*](../secgloss/c-gly.md)Active Directory.</span><span class="sxs-lookup"><span data-stu-id="87c0b-104">The **CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION** enumeration type indicates the location to be searched for an Active Directory [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="87c0b-105">Membri</span><span class="sxs-lookup"><span data-stu-id="87c0b-105">Members</span></span>



| <span data-ttu-id="87c0b-106">Membro</span><span class="sxs-lookup"><span data-stu-id="87c0b-106">Member</span></span>                               | <span data-ttu-id="87c0b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87c0b-107">Description</span></span>                                  | <span data-ttu-id="87c0b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="87c0b-108">Value</span></span> |
|--------------------------------------|----------------------------------------------|-------|
| <span data-ttu-id="87c0b-109">**\_ricerca CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="87c0b-109">**CAPICOM\_SEARCH\_ANY**</span></span>             | <span data-ttu-id="87c0b-110">Cerca tutti i percorsi disponibili.</span><span class="sxs-lookup"><span data-stu-id="87c0b-110">Searches all available locations.</span></span><br/> | <span data-ttu-id="87c0b-111">0</span><span class="sxs-lookup"><span data-stu-id="87c0b-111">0</span></span>     |
| <span data-ttu-id="87c0b-112">**\_catalogo globale di ricerca \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="87c0b-112">**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</span></span> | <span data-ttu-id="87c0b-113">Esegue la ricerca solo nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="87c0b-113">Searches only the global catalog.</span></span><br/> | <span data-ttu-id="87c0b-114">1</span><span class="sxs-lookup"><span data-stu-id="87c0b-114">1</span></span>     |
| <span data-ttu-id="87c0b-115">**\_dominio predefinito di ricerca di CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87c0b-115">**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</span></span> | <span data-ttu-id="87c0b-116">Cerca solo il dominio predefinito.</span><span class="sxs-lookup"><span data-stu-id="87c0b-116">Searches only the default domain.</span></span><br/> | <span data-ttu-id="87c0b-117">2</span><span class="sxs-lookup"><span data-stu-id="87c0b-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="87c0b-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="87c0b-118">Remarks</span></span>

<span data-ttu-id="87c0b-119">Questo tipo di enumerazione viene usato dalla proprietà seguente:</span><span class="sxs-lookup"><span data-stu-id="87c0b-119">This enumeration type is used by the following property:</span></span>

-   [<span data-ttu-id="87c0b-120">**Settings. ActiveDirectorySearchLocation**</span><span class="sxs-lookup"><span data-stu-id="87c0b-120">**Settings.ActiveDirectorySearchLocation**</span></span>](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a><span data-ttu-id="87c0b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87c0b-121">Requirements</span></span>



| <span data-ttu-id="87c0b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="87c0b-122">Requirement</span></span> | <span data-ttu-id="87c0b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="87c0b-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87c0b-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="87c0b-124">Redistributable</span></span><br/> | <span data-ttu-id="87c0b-125">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="87c0b-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="87c0b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87c0b-126">Header</span></span><br/>          | <dl> <span data-ttu-id="87c0b-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="87c0b-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 
