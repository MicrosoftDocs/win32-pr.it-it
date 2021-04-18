---
description: Imposta o Recupera il percorso di ricerca Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Proprietà Settings. ActiveDirectorySearchLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329465"
---
# <a name="settingsactivedirectorysearchlocation-property"></a><span data-ttu-id="fe24a-103">Proprietà Settings. ActiveDirectorySearchLocation</span><span class="sxs-lookup"><span data-stu-id="fe24a-103">Settings.ActiveDirectorySearchLocation property</span></span>

<span data-ttu-id="fe24a-104">\[La proprietà **ActiveDirectorySearchLocation** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]</span><span class="sxs-lookup"><span data-stu-id="fe24a-104">\[The **ActiveDirectorySearchLocation** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="fe24a-105">La proprietà **ActiveDirectorySearchLocation** imposta o Recupera il percorso di ricerca Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fe24a-105">The **ActiveDirectorySearchLocation** property sets or retrieves the Active Directory search location.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe24a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe24a-106">Syntax</span></span>


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="fe24a-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fe24a-107">Property value</span></span>

<span data-ttu-id="fe24a-108">Valore dell'enumerazione del [**\_ percorso di ricerca di \_ Active \_ directory \_ di CAPICOM**](capicom-active-directory-search-location.md) che specifica il percorso di ricerca.</span><span class="sxs-lookup"><span data-stu-id="fe24a-108">A value of the [**CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION**](capicom-active-directory-search-location.md) enumeration that specifies the search location.</span></span> <span data-ttu-id="fe24a-109">Il valore predefinito è CAPICOM \_ ricerca \_ any.</span><span class="sxs-lookup"><span data-stu-id="fe24a-109">The default value is CAPICOM\_SEARCH\_ANY.</span></span> <span data-ttu-id="fe24a-110">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="fe24a-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="fe24a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="fe24a-111">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="fe24a-112">Significato</span><span class="sxs-lookup"><span data-stu-id="fe24a-112">Meaning</span></span>                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <span data-ttu-id="fe24a-113"><dt>**\_ricerca CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe24a-113"><dt>**CAPICOM\_SEARCH\_ANY**</dt></span></span> </dl>                                   | <span data-ttu-id="fe24a-114">Cerca tutti i percorsi disponibili.</span><span class="sxs-lookup"><span data-stu-id="fe24a-114">Search all available locations.</span></span><br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <span data-ttu-id="fe24a-115"><dt>**\_dominio predefinito di ricerca di CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe24a-115"><dt>**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="fe24a-116">Eseguire la ricerca solo nel dominio predefinito.</span><span class="sxs-lookup"><span data-stu-id="fe24a-116">Search only the default domain.</span></span><br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <span data-ttu-id="fe24a-117"><dt>**\_catalogo globale di ricerca \_ CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe24a-117"><dt>**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</dt></span></span> </dl> | <span data-ttu-id="fe24a-118">Eseguire la ricerca solo nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="fe24a-118">Search only the global catalog.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fe24a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe24a-119">Requirements</span></span>



| <span data-ttu-id="fe24a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe24a-120">Requirement</span></span> | <span data-ttu-id="fe24a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fe24a-121">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe24a-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fe24a-122">Redistributable</span></span><br/> | <span data-ttu-id="fe24a-123">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe24a-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fe24a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fe24a-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="fe24a-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe24a-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe24a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe24a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe24a-127">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="fe24a-127">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




