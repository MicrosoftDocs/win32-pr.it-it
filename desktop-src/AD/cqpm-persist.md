---
title: Messaggio CQPM_PERSIST (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per consentire alla pagina di leggere o scrivere dati di query dalla memoria persistente.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_PERSIST Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048307"
---
# <a name="cqpm_persist-message"></a><span data-ttu-id="14dac-104">CQPM \_ messaggio permanente</span><span class="sxs-lookup"><span data-stu-id="14dac-104">CQPM\_PERSIST message</span></span>

<span data-ttu-id="14dac-105">Il messaggio di **\_ persistenza CQPM** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per consentire alla pagina di leggere o scrivere dati di query dalla memoria persistente.</span><span class="sxs-lookup"><span data-stu-id="14dac-105">The **CQPM\_PERSIST** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page to read or write query data from persistent memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="14dac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14dac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14dac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14dac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14dac-108">Contiene un valore diverso da zero per leggere i dati della query o zero per scrivere i dati della query.</span><span class="sxs-lookup"><span data-stu-id="14dac-108">Contains nonzero to read the query data or zero to write the query data.</span></span>

</dd> <dt>

<span data-ttu-id="14dac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14dac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14dac-110">Puntatore a un'interfaccia [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) da cui devono essere letti o scritti i dati della query.</span><span class="sxs-lookup"><span data-stu-id="14dac-110">Pointer to an [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) interface that the query data should be read from or written to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14dac-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14dac-111">Return value</span></span>

<span data-ttu-id="14dac-112">Restituisce **\_ OK** se l'esito è positivo o un codice di errore **HRESULT** standard.</span><span class="sxs-lookup"><span data-stu-id="14dac-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="14dac-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14dac-113">Requirements</span></span>



| <span data-ttu-id="14dac-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="14dac-114">Requirement</span></span> | <span data-ttu-id="14dac-115">Valore</span><span class="sxs-lookup"><span data-stu-id="14dac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14dac-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14dac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="14dac-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14dac-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="14dac-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14dac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="14dac-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14dac-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="14dac-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14dac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="14dac-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="14dac-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14dac-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14dac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14dac-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="14dac-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="14dac-124">**IPersistQuery**</span><span class="sxs-lookup"><span data-stu-id="14dac-124">**IPersistQuery**</span></span>](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

