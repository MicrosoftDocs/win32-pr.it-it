---
description: Recupera gli stili per un attributo specificato.
ms.assetid: 206c69b9-981b-49ef-9f71-1c65e08637bb
title: PIMEStyleFromAttr (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PIMEStyleFromAttr
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 27673ebb74c1dca3e686542a541735cfc515bee9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325101"
---
# <a name="pimestylefromattr-function"></a><span data-ttu-id="51769-103">PIMEStyleFromAttr (funzione)</span><span class="sxs-lookup"><span data-stu-id="51769-103">PIMEStyleFromAttr function</span></span>

<span data-ttu-id="51769-104">Recupera gli stili per un attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="51769-104">Retrieves styles for a given attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="51769-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51769-105">Syntax</span></span>


```C++
const IMESTYLE* __cdecl PIMEStyleFromAttr(
  _In_ const  UINT attr
);
```



## <a name="parameters"></a><span data-ttu-id="51769-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51769-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51769-107">*attr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51769-107">*attr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51769-108">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="51769-108">This parameter can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="51769-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR \_ FIXEDCONVERTED** (5)</span><span class="sxs-lookup"><span data-stu-id="51769-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR\_FIXEDCONVERTED** (5)</span></span>
</dt> <dt>

<span data-ttu-id="51769-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR \_ INPUT** (0)</span><span class="sxs-lookup"><span data-stu-id="51769-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR\_INPUT** (0)</span></span>
</dt> <dt>

<span data-ttu-id="51769-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR \_ \_Errore di input** (4)</span><span class="sxs-lookup"><span data-stu-id="51769-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR\_INPUT\_ERROR** (4)</span></span>
</dt> <dt>

<span data-ttu-id="51769-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR \_ MASSIMO** (5)</span><span class="sxs-lookup"><span data-stu-id="51769-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR\_MAX** (5)</span></span>
</dt> <dt>

<span data-ttu-id="51769-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR \_ MIN** (0)</span><span class="sxs-lookup"><span data-stu-id="51769-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR\_MIN** (0)</span></span>
</dt> <dt>

<span data-ttu-id="51769-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR \_ DESTINAZIONE \_ convertita** (1)</span><span class="sxs-lookup"><span data-stu-id="51769-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR\_TARGET\_CONVERTED** (1)</span></span>
</dt> <dt>

<span data-ttu-id="51769-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR \_ \_NOTCONVERTED di destinazione** (4)</span><span class="sxs-lookup"><span data-stu-id="51769-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR\_TARGET\_NOTCONVERTED** (4)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51769-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51769-116">Return value</span></span>

<span data-ttu-id="51769-117">Restituisce un puntatore a una struttura **IMESTYLE** che rappresenta le impostazioni di colore e non colore.</span><span class="sxs-lookup"><span data-stu-id="51769-117">Returns a pointer to an **IMESTYLE** structure representing the color and non-color settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="51769-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="51769-118">Remarks</span></span>

<span data-ttu-id="51769-119">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="51769-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="51769-120">La struttura **IMESTYLE** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="51769-120">The **IMESTYLE** structure is defined as follows:</span></span>

``` syntax
typedef struct {
    union {
        GRFSTY  grfsty;
        struct {
            UINT    fBold:1;
            UINT    fItalic:1;
            UINT    fUl:1;
            UINT    idUl:(sizeof(UINT) * 8 - 3);
        };
    };

    union {
        IMECOLORSTY colorstyText;
        struct {
            UINT    colorIdText;
            union {
                COLORREF    rgbText;
                UINT        colorWinText;
                UINT        colorSpecText;
                UINT        colorFundText;
            };
        };
    };

    union {
        IMECOLORSTY colorstyBack;
        struct {
            UINT    colorIdBack;
            union {
                COLORREF    rgbBack;
                UINT        colorWinBack;
                UINT        colorSpecBack;
                UINT        colorFundBack;
            };
        };
    };

    union {
        IMECOLORSTY colorstyUl;
        struct {
            UINT    colorIdUl;
            union {
                COLORREF    rgbUl;
                UINT        colorWinUl;
                UINT        colorSpecUl;
                UINT        colorFundUl;
            };
        };
    };
} IMESTYLE;
```

## <a name="requirements"></a><span data-ttu-id="51769-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51769-121">Requirements</span></span>



| <span data-ttu-id="51769-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="51769-122">Requirement</span></span> | <span data-ttu-id="51769-123">Valore</span><span class="sxs-lookup"><span data-stu-id="51769-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51769-124">DLL</span><span class="sxs-lookup"><span data-stu-id="51769-124">DLL</span></span><br/> | <dl> <span data-ttu-id="51769-125"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51769-125"><dt>Imeshare.dll</dt></span></span> </dl> |



 

 
