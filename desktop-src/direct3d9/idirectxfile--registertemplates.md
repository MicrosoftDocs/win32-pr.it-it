---
description: Registra i modelli personalizzati. Deprecato.
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: 'Metodo IDirectXFile:: RegisterTemplates (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 683a495398e7fe0718ee0642c7760b0a8590538c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322542"
---
# <a name="idirectxfileregistertemplates-method"></a><span data-ttu-id="aa655-104">Metodo IDirectXFile:: RegisterTemplates</span><span class="sxs-lookup"><span data-stu-id="aa655-104">IDirectXFile::RegisterTemplates method</span></span>

<span data-ttu-id="aa655-105">Registra i modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="aa655-105">Registers custom templates.</span></span> <span data-ttu-id="aa655-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="aa655-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa655-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa655-107">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="aa655-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa655-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa655-109">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa655-109">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa655-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa655-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aa655-111">Puntatore a un buffer costituito da un file DirectX in formato testo o binario che contiene modelli.</span><span class="sxs-lookup"><span data-stu-id="aa655-111">Pointer to a buffer consisting of a DirectX file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="aa655-112">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa655-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa655-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa655-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aa655-114">Dimensioni del buffer a cui punta pvData in byte.</span><span class="sxs-lookup"><span data-stu-id="aa655-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa655-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa655-115">Return value</span></span>

<span data-ttu-id="aa655-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aa655-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aa655-117">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aa655-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="aa655-118">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR BADVALUE \_ , DXFILEERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="aa655-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADVALUE, DXFILEERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa655-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa655-119">Remarks</span></span>

<span data-ttu-id="aa655-120">Il seguente frammento di codice fornisce una chiamata di esempio a **RegisterTemplates** e il contenuto di esempio per il buffer a cui punta pvData.</span><span class="sxs-lookup"><span data-stu-id="aa655-120">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which pvData points.</span></span>


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



<span data-ttu-id="aa655-121">Tutti i modelli devono specificare un nome e un identificatore univoco universale (UUID).</span><span class="sxs-lookup"><span data-stu-id="aa655-121">All templates must specify a name and a Universally Unique Identifier (UUID).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa655-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa655-122">Requirements</span></span>



| <span data-ttu-id="aa655-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa655-123">Requirement</span></span> | <span data-ttu-id="aa655-124">Valore</span><span class="sxs-lookup"><span data-stu-id="aa655-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa655-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa655-125">Header</span></span><br/>  | <dl> <span data-ttu-id="aa655-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa655-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa655-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa655-127">Library</span></span><br/> | <dl> <span data-ttu-id="aa655-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa655-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa655-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa655-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa655-130">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="aa655-130">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
