---
title: Enumerazione WMDM_TAG_DATATYPE
description: Il \_ \_ tipo di enumerazione WMDM Tag DataType definisce un tipo di dati.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- Enumerazione WMDM_TAG_DATATYPE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325009"
---
# <a name="wmdm_tag_datatype-enumeration"></a><span data-ttu-id="c75ef-104">\_ \_ Enumerazione DataType Tag WMDM</span><span class="sxs-lookup"><span data-stu-id="c75ef-104">WMDM\_TAG\_DATATYPE enumeration</span></span>

<span data-ttu-id="c75ef-105">Il tipo di enumerazione **WMDM \_ tag \_ DataType** definisce un tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="c75ef-105">The **WMDM\_TAG\_DATATYPE** enumeration type defines a data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75ef-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c75ef-106">Syntax</span></span>


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a><span data-ttu-id="c75ef-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="c75ef-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c75ef-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c75ef-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c75ef-109">Specifica un valore **DWORD** a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="c75ef-109">Specifies a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="c75ef-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**\_stringa di tipo WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="c75ef-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="c75ef-111">Specifica una stringa Unicode con terminazione null (2 byte per carattere).</span><span class="sxs-lookup"><span data-stu-id="c75ef-111">Specifies a null-terminated Unicode string (2 bytes per character).</span></span>

</dd> <dt>

<span data-ttu-id="c75ef-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**\_binario di tipo WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="c75ef-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="c75ef-113">Specifica una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="c75ef-113">Specifies an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c75ef-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**\_tipo WMDM \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c75ef-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="c75ef-115">Specifica un valore booleano a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="c75ef-115">Specifies a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="c75ef-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM \_ tipo \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="c75ef-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c75ef-117">Specifica un valore **QWORD** a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="c75ef-117">Specifies an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="c75ef-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM \_ digitare \_ Word**</span><span class="sxs-lookup"><span data-stu-id="c75ef-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="c75ef-119">Specifica un valore **Word** a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="c75ef-119">Specifies a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="c75ef-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID di tipo WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="c75ef-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="c75ef-121">Specifica un GUID a 128 bit (16 byte).</span><span class="sxs-lookup"><span data-stu-id="c75ef-121">Specifies a 128-bit (16-byte) GUID.</span></span>

</dd> <dt>

<span data-ttu-id="c75ef-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM \_ tipo di \_ dati**</span><span class="sxs-lookup"><span data-stu-id="c75ef-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM\_TYPE\_DATE**</span></span>
</dt> <dd>

<span data-ttu-id="c75ef-123">Specifica una data.</span><span class="sxs-lookup"><span data-stu-id="c75ef-123">Specifies a date.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c75ef-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c75ef-124">Requirements</span></span>



| <span data-ttu-id="c75ef-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c75ef-125">Requirement</span></span> | <span data-ttu-id="c75ef-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c75ef-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c75ef-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c75ef-127">Header</span></span><br/> | <dl> <span data-ttu-id="c75ef-128"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c75ef-128"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c75ef-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c75ef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75ef-130">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="c75ef-130">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





