---
title: Enumerazione WMDM_STORAGE_ENUM_MODE
description: Il \_ \_ \_ tipo di enumerazione WMDM storage enum Mode definisce il modo in cui deve essere enumerato il contenuto nell'archivio. Questa enumerazione viene utilizzata da IWMDMStorage3 SetEnumPreference.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- Enumerazione WMDM_STORAGE_ENUM_MODE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324759"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a><span data-ttu-id="64743-105">\_Enumerazione della \_ modalità enum di archiviazione WMDM \_</span><span class="sxs-lookup"><span data-stu-id="64743-105">WMDM\_STORAGE\_ENUM\_MODE enumeration</span></span>

<span data-ttu-id="64743-106">Il tipo di enumerazione **WMDM \_ storage \_ enum \_ mode** definisce il modo in cui deve essere enumerato il contenuto nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="64743-106">The **WMDM\_STORAGE\_ENUM\_MODE** enumeration type defines how the content on the storage is to be enumerated.</span></span> <span data-ttu-id="64743-107">Questa enumerazione viene utilizzata da [**IWMDMStorage3:: SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span><span class="sxs-lookup"><span data-stu-id="64743-107">This enumeration is used by [**IWMDMStorage3::SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span></span>

## <a name="syntax"></a><span data-ttu-id="64743-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64743-108">Syntax</span></span>


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a><span data-ttu-id="64743-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="64743-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="64743-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**modalità di enumerazione non \_ \_ elaborata**</span><span class="sxs-lookup"><span data-stu-id="64743-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**ENUM\_MODE\_RAW**</span></span>
</dt> <dd>

<span data-ttu-id="64743-111">Enumera il contenuto nell'archiviazione così come è organizzato nel file system dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="64743-111">Enumerates content on the storage just as it is organized in the file system of the storage.</span></span>

<span data-ttu-id="64743-112">**\_modalità enum \_ Usa \_ \_ pref dispositivo**</span><span class="sxs-lookup"><span data-stu-id="64743-112">**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>

<span data-ttu-id="64743-113">Enumera il contenuto nell'archiviazione in base alla preferenza del dispositivo come indicato dal parametro del dispositivo *UseMetadataViews* .</span><span class="sxs-lookup"><span data-stu-id="64743-113">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="64743-114">**\_ \_ viste dei metadati in modalità enum \_**</span><span class="sxs-lookup"><span data-stu-id="64743-114">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="64743-115">Enumera il contenuto nell'archivio organizzando il contenuto in base a una visualizzazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="64743-115">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="64743-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**\_modalità enum \_ Usa \_ \_ pref dispositivo**</span><span class="sxs-lookup"><span data-stu-id="64743-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>
</dt> <dd>

<span data-ttu-id="64743-117">Enumera il contenuto nell'archiviazione in base alla preferenza del dispositivo come indicato dal parametro del dispositivo *UseMetadataViews* .</span><span class="sxs-lookup"><span data-stu-id="64743-117">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="64743-118">**\_ \_ viste dei metadati in modalità enum \_**</span><span class="sxs-lookup"><span data-stu-id="64743-118">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="64743-119">Enumera il contenuto nell'archivio organizzando il contenuto in base a una visualizzazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="64743-119">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="64743-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**\_ \_ viste dei metadati in modalità enum \_**</span><span class="sxs-lookup"><span data-stu-id="64743-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**ENUM\_MODE\_METADATA\_VIEWS**</span></span>
</dt> <dd>

<span data-ttu-id="64743-121">Enumera il contenuto nell'archivio organizzando il contenuto in base a una visualizzazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="64743-121">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64743-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64743-122">Requirements</span></span>



| <span data-ttu-id="64743-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="64743-123">Requirement</span></span> | <span data-ttu-id="64743-124">Valore</span><span class="sxs-lookup"><span data-stu-id="64743-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="64743-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64743-125">Header</span></span><br/> | <dl> <span data-ttu-id="64743-126"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64743-126"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64743-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64743-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64743-128">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="64743-128">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





