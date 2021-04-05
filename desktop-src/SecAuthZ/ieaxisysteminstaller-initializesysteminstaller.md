---
description: Installa l'oggetto ActiveX specificato.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'Metodo IeAxiSystemInstaller:: InitializeSystemInstaller'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884457"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a><span data-ttu-id="2f389-103">Metodo IeAxiSystemInstaller:: InitializeSystemInstaller</span><span class="sxs-lookup"><span data-stu-id="2f389-103">IeAxiSystemInstaller::InitializeSystemInstaller method</span></span>

<span data-ttu-id="2f389-104">Il metodo **InitializeSystemInstaller** installa l'oggetto ActiveX specificato.</span><span class="sxs-lookup"><span data-stu-id="2f389-104">The **InitializeSystemInstaller** method installs the specified ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f389-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f389-105">Syntax</span></span>


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a><span data-ttu-id="2f389-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f389-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f389-107">*bstrURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f389-107">*bstrUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f389-108">URL dell'oggetto ActiveX da installare.</span><span class="sxs-lookup"><span data-stu-id="2f389-108">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="2f389-109">*dwClientPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f389-109">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f389-110">ID processo del processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="2f389-110">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="2f389-111">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f389-111">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f389-112">Puntatore a un'istanza dell'interfaccia [**IeAxiServiceCallback**](ieaxiservicecallback.md) che verifica se l'oggetto ActiveX può essere installato.</span><span class="sxs-lookup"><span data-stu-id="2f389-112">A pointer to an instance of the [**IeAxiServiceCallback**](ieaxiservicecallback.md) interface that verifies whether the ActiveX object is allowed to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="2f389-113">*pbstrNonce* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f389-113">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f389-114">Contesto che può essere utilizzato per condividere le informazioni sullo stato nelle chiamate ad altri metodi utilizzati per verificare e scaricare l'oggetto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="2f389-114">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f389-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f389-115">Return value</span></span>

<span data-ttu-id="2f389-116">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2f389-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="2f389-117">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="2f389-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="2f389-118">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="2f389-118">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f389-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f389-119">Requirements</span></span>



| <span data-ttu-id="2f389-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f389-120">Requirement</span></span> | <span data-ttu-id="2f389-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2f389-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f389-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f389-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2f389-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="2f389-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2f389-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f389-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2f389-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2f389-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="2f389-126">IID</span><span class="sxs-lookup"><span data-stu-id="2f389-126">IID</span></span><br/>                      | <span data-ttu-id="2f389-127">IID \_ IeAxiSystemInstaller è definito come a50ea6f8-4764-4299-B309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="2f389-127">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="2f389-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f389-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f389-129">**IeAxiSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="2f389-129">**IeAxiSystemInstaller**</span></span>](ieaxisysteminstaller.md)
</dt> </dl>

 

