---
description: Funzione di callback utilizzata per notificare all'host le informazioni sui file di origine associati a stack.
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ISourceFileInfoCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a60122615cf15e9ed39ae7809e574c4d3d0c1146
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125541"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span data-ttu-id="50e14-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>Metodo ISourceFileInfoCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="50e14-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback::ResultCallback method</span></span>

<span data-ttu-id="50e14-104">Funzione di callback utilizzata per notificare all'host le informazioni sui file di origine associati a stack.</span><span class="sxs-lookup"><span data-stu-id="50e14-104">A callback function used to notify the host of information about source files associated with the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e14-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50e14-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="50e14-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50e14-106">Parameters</span></span>

<span data-ttu-id="50e14-107">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="50e14-107">*count* </span></span>  
<span data-ttu-id="50e14-108">Numero di file di origine restituiti.</span><span class="sxs-lookup"><span data-stu-id="50e14-108">The number of source files returned.</span></span>

<span data-ttu-id="50e14-109">*\_sourceFileInfoBuffer count0* </span><span class="sxs-lookup"><span data-stu-id="50e14-109">*count0\_sourceFileInfoBuffer* </span></span>  
<span data-ttu-id="50e14-110">File di origine.</span><span class="sxs-lookup"><span data-stu-id="50e14-110">The source files.</span></span>

## <a name="return-value"></a><span data-ttu-id="50e14-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50e14-111">Return value</span></span>

<span data-ttu-id="50e14-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="50e14-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50e14-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="50e14-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e14-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50e14-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="50e14-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50e14-115">Header</span></span></p></td><td><span data-ttu-id="50e14-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="50e14-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="50e14-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="50e14-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="50e14-118">**ISourceFileInfoCallback**</span><span class="sxs-lookup"><span data-stu-id="50e14-118">**ISourceFileInfoCallback**</span></span>](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
