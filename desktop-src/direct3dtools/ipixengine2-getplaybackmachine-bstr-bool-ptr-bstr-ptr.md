---
description: Ottiene informazioni sul computer di riproduzione corrente.
MS-HAID: vspixengine.IPixEngine2\_GetPlaybackMachine\_BSTR\_BOOL\_ptr\_BSTR\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine2:: GetPlaybackMachine'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D6C3C391-F039-4A5A-AA88-87A3624ECAD2
api_name:
- IPixEngine2.GetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c572d1a87fb537fd53a7f3e8f8048d1046980b20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304339"
---
# <a name="span-idvspixengineipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptrspanipixengine2getplaybackmachine-method"></a><span data-ttu-id="a3b95-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>Metodo IPixEngine2:: GetPlaybackMachine</span><span class="sxs-lookup"><span data-stu-id="a3b95-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>IPixEngine2::GetPlaybackMachine method</span></span>

<span data-ttu-id="a3b95-104">Ottiene informazioni sul computer di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="a3b95-104">Gets information about the current playback machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3b95-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3b95-105">Syntax</span></span>


```C++
HRESULT GetPlaybackMachine(
   BSTR   logFile,
   BOOL * pUseAuthentication,
   BSTR * pMachine
);
```

## <a name="parameters"></a><span data-ttu-id="a3b95-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3b95-106">Parameters</span></span>

<span data-ttu-id="a3b95-107">*logFile* </span><span class="sxs-lookup"><span data-stu-id="a3b95-107">*logFile* </span></span>  
<span data-ttu-id="a3b95-108">Stringa COM contenente il nome del log di grafica associato.</span><span class="sxs-lookup"><span data-stu-id="a3b95-108">A COM string containing the name of the associated graphics log.</span></span>

<span data-ttu-id="a3b95-109">*pUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="a3b95-109">*pUseAuthentication* </span></span>  
<span data-ttu-id="a3b95-110">In caso di restituzione, true se la connessione utilizza l'autenticazione di; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="a3b95-110">On return, true if the connection uses authentication; otherwise, false.</span></span>

<span data-ttu-id="a3b95-111">*pMachine* </span><span class="sxs-lookup"><span data-stu-id="a3b95-111">*pMachine* </span></span>  
<span data-ttu-id="a3b95-112">Al ritorno, stringa COM contenente il nome del computer di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a3b95-112">On return, a COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3b95-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3b95-113">Return value</span></span>

<span data-ttu-id="a3b95-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a3b95-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3b95-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3b95-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3b95-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3b95-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a3b95-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3b95-117">Header</span></span></p></td><td><span data-ttu-id="a3b95-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a3b95-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a3b95-119"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a3b95-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a3b95-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="a3b95-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
