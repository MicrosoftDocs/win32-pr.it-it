---
title: Tipi di modifica degli attributi ADSI (IADs. h)
description: Usato con il membro dwControlCode della struttura di informazioni di ADS \_ attr \_ per specificare il tipo di operazione da eseguire quando un attributo viene modificato con il metodo SetObjectAttributes di IDirectoryObject.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- tipi di modifica degli attributi ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048076"
---
# <a name="adsi-attribute-modification-types"></a><span data-ttu-id="36a09-104">Tipi di modifica degli attributi ADSI</span><span class="sxs-lookup"><span data-stu-id="36a09-104">ADSI Attribute Modification Types</span></span>

<span data-ttu-id="36a09-105">Le costanti seguenti vengono usate con il membro **dwControlCode** della struttura [**di \_ \_ informazioni di ADS attr**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) per specificare il tipo di operazione da eseguire quando un attributo viene modificato con il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="36a09-105">The following constants are used with the **dwControlCode** member of [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure to specify the type of operation to be performed when an attribute is modified with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="36a09-106">Per ulteriori informazioni sull'utilizzo di questi valori, vedere [modifica degli attributi con ADSI](modifying-attributes-with-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="36a09-106">For more information about using these values, see [Modifying Attributes with ADSI](modifying-attributes-with-adsi.md).</span></span>

<dl> <dt>

<span data-ttu-id="36a09-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**Clear degli annunci \_ attr \_**</span><span class="sxs-lookup"><span data-stu-id="36a09-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS\_ATTR\_CLEAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a09-108">1</span><span class="sxs-lookup"><span data-stu-id="36a09-108">1</span></span>
</dt> <dt>



<span data-ttu-id="36a09-109">Causa la rimozione di tutti i valori di attributo da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="36a09-109">Causes all attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36a09-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_aggiornamento attr \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="36a09-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS\_ATTR\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a09-111">2</span><span class="sxs-lookup"><span data-stu-id="36a09-111">2</span></span>
</dt> <dt>



<span data-ttu-id="36a09-112">Comporta l'aggiornamento dei valori di attributo specificati.</span><span class="sxs-lookup"><span data-stu-id="36a09-112">Causes the specified attribute values to be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36a09-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**\_accodamento degli annunci attr \_**</span><span class="sxs-lookup"><span data-stu-id="36a09-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS\_ATTR\_APPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a09-114">3</span><span class="sxs-lookup"><span data-stu-id="36a09-114">3</span></span>
</dt> <dt>



<span data-ttu-id="36a09-115">Consente di accodare i valori di attributo specificati ai valori degli attributi esistenti.</span><span class="sxs-lookup"><span data-stu-id="36a09-115">Causes the specified attribute values to be appended to the existing attribute values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36a09-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**eliminazione degli annunci \_ attr \_**</span><span class="sxs-lookup"><span data-stu-id="36a09-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS\_ATTR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a09-117">4</span><span class="sxs-lookup"><span data-stu-id="36a09-117">4</span></span>
</dt> <dt>



<span data-ttu-id="36a09-118">Determina la rimozione dei valori di attributo specificati da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="36a09-118">Causes the specified attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36a09-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="36a09-119">Remarks</span></span>

<span data-ttu-id="36a09-120">Queste costanti sono progettate per essere usate con la struttura [**di \_ \_ informazioni attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) nel metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="36a09-120">These constants are intended to be used with the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure in the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="36a09-121">Queste costanti non devono essere confuse con i membri dell' [**enumerazione \_ \_ \_ enum dell'operazione della proprietà ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , che devono essere usati con il metodo [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="36a09-121">These constants should not be confused with members of the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration, which are intended to be used with the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="36a09-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36a09-122">Requirements</span></span>



| <span data-ttu-id="36a09-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="36a09-123">Requirement</span></span> | <span data-ttu-id="36a09-124">Valore</span><span class="sxs-lookup"><span data-stu-id="36a09-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="36a09-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36a09-125">Minimum supported client</span></span><br/> | <span data-ttu-id="36a09-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36a09-126">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="36a09-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36a09-127">Minimum supported server</span></span><br/> | <span data-ttu-id="36a09-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36a09-128">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="36a09-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36a09-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="36a09-130"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="36a09-130"><dt>Iads.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a09-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36a09-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a09-132">**\_info attr \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="36a09-132">**ADS\_ATTR\_INFO**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[<span data-ttu-id="36a09-133">**IDirectoryObject::SetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="36a09-133">**IDirectoryObject::SetObjectAttributes**</span></span>](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="36a09-134">Modifica degli attributi con ADSI</span><span class="sxs-lookup"><span data-stu-id="36a09-134">Modifying Attributes with ADSI</span></span>](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





