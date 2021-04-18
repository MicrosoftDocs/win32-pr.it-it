---
description: Definisce le modalità di mapping a un ID di classe.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Enumerazione TYSPEC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: b4c8cf38a8f99458e76cabc726aa39ad01a71ebc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324439"
---
# <a name="tyspec-enumeration"></a><span data-ttu-id="3b8fb-103">Enumerazione TYSPEC</span><span class="sxs-lookup"><span data-stu-id="3b8fb-103">TYSPEC enumeration</span></span>

<span data-ttu-id="3b8fb-104">Definisce le modalità di mapping a un ID di classe.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-104">Defines ways of mapping to a class ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b8fb-105">Syntax</span></span>


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a><span data-ttu-id="3b8fb-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="3b8fb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3b8fb-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="3b8fb-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC\_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="3b8fb-108">CLSID.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-108">A CLSID.</span></span>

</dd> <dt>

<span data-ttu-id="3b8fb-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**\_FILEEXT TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="3b8fb-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC\_FILEEXT**</span></span>
</dt> <dd>

<span data-ttu-id="3b8fb-110">Estensione di file.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-110">A file name extension.</span></span> <span data-ttu-id="3b8fb-111">Questo valore non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-111">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="3b8fb-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**\_MIMETYPE TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="3b8fb-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC\_MIMETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="3b8fb-113">Tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-113">A MIME type.</span></span> <span data-ttu-id="3b8fb-114">Questo valore non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-114">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="3b8fb-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**\_nome file TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="3b8fb-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC\_FILENAME**</span></span>
</dt> <dd>

<span data-ttu-id="3b8fb-116">Nome file.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-116">A file name.</span></span> <span data-ttu-id="3b8fb-117">Questo valore non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-117">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="3b8fb-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**\_ProgID TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="3b8fb-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC\_PROGID**</span></span>
</dt> <dd>

<span data-ttu-id="3b8fb-119">PROGID.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-119">A PROGID.</span></span> <span data-ttu-id="3b8fb-120">Questo valore non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-120">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="3b8fb-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PackageName**</span><span class="sxs-lookup"><span data-stu-id="3b8fb-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC\_PACKAGENAME**</span></span>
</dt> <dd>

<span data-ttu-id="3b8fb-122">Nome del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-122">A package name.</span></span> <span data-ttu-id="3b8fb-123">Questo valore non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-123">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="3b8fb-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**\_ObjectID TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="3b8fb-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC\_OBJECTID**</span></span>
</dt> <dd>

<span data-ttu-id="3b8fb-125">ID di oggetto.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-125">An object ID.</span></span> <span data-ttu-id="3b8fb-126">Questo valore non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="3b8fb-126">This value is not currently supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b8fb-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b8fb-127">Remarks</span></span>

<span data-ttu-id="3b8fb-128">L'Unione **uCLSSPEC** è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="3b8fb-128">The **uCLSSPEC** union is defined as follows:</span></span>

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a><span data-ttu-id="3b8fb-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b8fb-129">Requirements</span></span>



| <span data-ttu-id="3b8fb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b8fb-130">Requirement</span></span> | <span data-ttu-id="3b8fb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3b8fb-131">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8fb-132">IDL</span><span class="sxs-lookup"><span data-stu-id="3b8fb-132">IDL</span></span><br/> | <dl> <span data-ttu-id="3b8fb-133"><dt>Wtypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b8fb-133"><dt>Wtypes.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8fb-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b8fb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8fb-135">**Coinstallazione**</span><span class="sxs-lookup"><span data-stu-id="3b8fb-135">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
