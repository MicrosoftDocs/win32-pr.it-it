---
description: Imposta il computer di riproduzione corrente per il log di grafica specificato.
MS-HAID: vspixengine.IPixEngine2\_SetPlaybackMachine\_BSTR\_BOOL\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine2:: SetPlaybackMachine'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 181EE044-1FC4-484B-AE63-C33BC627C3B7
api_name:
- IPixEngine2.SetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d7366da4aa999828309136900edfe725af4f622
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522714"
---
# <a name="span-idvspixengineipixengine2_setplaybackmachine_bstr_bool_bstrspanipixengine2setplaybackmachine-method"></a><span data-ttu-id="60542-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>Metodo IPixEngine2:: SetPlaybackMachine</span><span class="sxs-lookup"><span data-stu-id="60542-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2::SetPlaybackMachine method</span></span>

<span data-ttu-id="60542-104">Imposta il computer di riproduzione corrente per il log di grafica specificato.</span><span class="sxs-lookup"><span data-stu-id="60542-104">Sets the current playback machine for the specified graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="60542-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60542-105">Syntax</span></span>


```C++
HRESULT SetPlaybackMachine(
   BSTR logFile,
   BOOL bUseAuthentication,
   BSTR machine
);
```

## <a name="parameters"></a><span data-ttu-id="60542-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60542-106">Parameters</span></span>

<span data-ttu-id="60542-107">*logFile* </span><span class="sxs-lookup"><span data-stu-id="60542-107">*logFile* </span></span>  
<span data-ttu-id="60542-108">Stringa COM che costituisce il nome del log di grafica.</span><span class="sxs-lookup"><span data-stu-id="60542-108">A COM string contianing the name of the graphics log.</span></span>

<span data-ttu-id="60542-109">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="60542-109">*bUseAuthentication* </span></span>  
<span data-ttu-id="60542-110">true per utilizzare l'autenticazione; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="60542-110">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="60542-111">*macchina* </span><span class="sxs-lookup"><span data-stu-id="60542-111">*machine* </span></span>  
<span data-ttu-id="60542-112">Stringa COM contenente il nome del computer di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="60542-112">A COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="60542-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60542-113">Return value</span></span>

<span data-ttu-id="60542-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="60542-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="60542-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60542-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="60542-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60542-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="60542-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60542-117">Header</span></span></p></td><td><span data-ttu-id="60542-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="60542-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="60542-119"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="60542-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="60542-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="60542-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
