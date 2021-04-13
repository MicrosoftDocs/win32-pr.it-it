---
description: Richiede l'esecuzione di un'analisi offline con l'origine, il manifesto, i parametri e del frame specificati specificati.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IOfflineAnalysisRequest:: RequestOfflineAnalysisAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d027b9ec463c0bebfefca3ee7f9af4b50c514755
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401241"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span data-ttu-id="ff1f7-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>Metodo IOfflineAnalysisRequest:: RequestOfflineAnalysisAsync</span><span class="sxs-lookup"><span data-stu-id="ff1f7-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest::RequestOfflineAnalysisAsync method</span></span>

<span data-ttu-id="ff1f7-104">Richiede l'esecuzione di un'analisi offline con l'origine, il manifesto, i parametri e del frame specificati specificati.</span><span class="sxs-lookup"><span data-stu-id="ff1f7-104">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff1f7-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="ff1f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff1f7-106">Parameters</span></span>

<span data-ttu-id="ff1f7-107">*analysisSource* </span><span class="sxs-lookup"><span data-stu-id="ff1f7-107">*analysisSource* </span></span>  
<span data-ttu-id="ff1f7-108">Specifica in cui l'origine dell'analisi proviene dai report memorizzati nella cache o dalla riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ff1f7-108">Specfies where the analysis source come from cached reports or from playback.</span></span>

<span data-ttu-id="ff1f7-109">*manifestXml* </span><span class="sxs-lookup"><span data-stu-id="ff1f7-109">*manifestXml* </span></span>  
<span data-ttu-id="ff1f7-110">Stringa COM contenente il percorso del file manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="ff1f7-110">A COM string containing the pathname of the XML manifest file.</span></span>

<span data-ttu-id="ff1f7-111">*parametersXml* </span><span class="sxs-lookup"><span data-stu-id="ff1f7-111">*parametersXml* </span></span>  
<span data-ttu-id="ff1f7-112">Stringa COM contenente il percorso del file dei parametri XML.</span><span class="sxs-lookup"><span data-stu-id="ff1f7-112">A COM string containing the pathname of the XML parameters file.</span></span>

<span data-ttu-id="ff1f7-113">*cookie* </span><span class="sxs-lookup"><span data-stu-id="ff1f7-113">*cookie* </span></span>  
<span data-ttu-id="ff1f7-114">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="ff1f7-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ff1f7-115">*captureFullFileName* </span><span class="sxs-lookup"><span data-stu-id="ff1f7-115">*captureFullFileName* </span></span>  
<span data-ttu-id="ff1f7-116">Stringa COM contenente il percorso assoluto del file di acquisizione (. vsglog).</span><span class="sxs-lookup"><span data-stu-id="ff1f7-116">A COM string containing the absolute pathname of the capture file (.vsglog).</span></span>

<span data-ttu-id="ff1f7-117">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="ff1f7-117">*frameNumber* </span></span>  
<span data-ttu-id="ff1f7-118">Frame specificato.</span><span class="sxs-lookup"><span data-stu-id="ff1f7-118">The specified frame.</span></span>

<span data-ttu-id="ff1f7-119">*outputFullFileName* </span><span class="sxs-lookup"><span data-stu-id="ff1f7-119">*outputFullFileName* </span></span>  
<span data-ttu-id="ff1f7-120">Stringa COM contenente il percorso assoluto del file in cui viene scritto l'output.</span><span class="sxs-lookup"><span data-stu-id="ff1f7-120">A COM string containing the absolute pathname of the file where output is written.</span></span>

<span data-ttu-id="ff1f7-121">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ff1f7-121">*requestCallback* </span></span>  
<span data-ttu-id="ff1f7-122">Indirizzo di un callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="ff1f7-122">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff1f7-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff1f7-123">Return value</span></span>

<span data-ttu-id="ff1f7-124">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ff1f7-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff1f7-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff1f7-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1f7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff1f7-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ff1f7-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff1f7-127">Header</span></span></p></td><td><span data-ttu-id="ff1f7-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ff1f7-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ff1f7-129"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ff1f7-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ff1f7-130">**IOfflineAnalysisRequest**</span><span class="sxs-lookup"><span data-stu-id="ff1f7-130">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
