---
description: "Metodo IMpeg2PsiParser::GetPatVersionNumber: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: Metodo IMpeg2PsiParser::GetPatVersionNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 978da4c7076bcf8ffe91bc2b9a4b2077d9d3d48a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089149"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="31ef3-104">Metodo IMpeg2PsiParser::GetPatVersionNumber</span><span class="sxs-lookup"><span data-stu-id="31ef3-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="31ef3-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="31ef3-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="31ef3-106">Non è un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="31ef3-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="31ef3-107">Il `GetPatVersionNumber` metodo recupera il campo del numero di versione da \_ PAT.</span><span class="sxs-lookup"><span data-stu-id="31ef3-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="31ef3-108">Un flusso di trasporto contiene al massimo un pat.</span><span class="sxs-lookup"><span data-stu-id="31ef3-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="31ef3-109">Il numero di versione viene incrementato ogni volta che le informazioni nella tabella vengono cambiate.</span><span class="sxs-lookup"><span data-stu-id="31ef3-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ef3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31ef3-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="31ef3-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="31ef3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ef3-112">*pPatVersion* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="31ef3-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31ef3-113">Puntatore a una variabile che riceve il campo del \_ numero di versione.</span><span class="sxs-lookup"><span data-stu-id="31ef3-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ef3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31ef3-114">Return value</span></span>

<span data-ttu-id="31ef3-115">Il metodo restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="31ef3-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="31ef3-116">I valori possibili includono, ma non sono limitati, i valori illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="31ef3-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="31ef3-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="31ef3-117">Return code</span></span>                                                                          | <span data-ttu-id="31ef3-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31ef3-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="31ef3-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="31ef3-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="31ef3-120">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="31ef3-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="31ef3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31ef3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ef3-122">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="31ef3-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="31ef3-123">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="31ef3-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




