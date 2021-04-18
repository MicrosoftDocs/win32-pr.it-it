---
title: Proprietà di dominio ITsSbClientConnection
description: Recupera un valore che indica il nome di dominio del client di Connessione Desktop remoto (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà di dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia ITsSbClientConnection
- Interfaccia ITsSbClientConnection Servizi Desktop remoto, proprietà del dominio
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302454"
---
# <a name="itssbclientconnectiondomain-property"></a><span data-ttu-id="a2206-106">ITsSbClientConnection::D Proprietà ominio</span><span class="sxs-lookup"><span data-stu-id="a2206-106">ITsSbClientConnection::Domain property</span></span>

<span data-ttu-id="a2206-107">Recupera un valore che indica il nome di dominio del client di Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="a2206-107">Retrieves a value that indicates the domain name of the Remote Desktop Connection (RDC) client.</span></span>

<span data-ttu-id="a2206-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a2206-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2206-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2206-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="a2206-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a2206-110">Property value</span></span>

<span data-ttu-id="a2206-111">Puntatore a una variabile **BSTR** che contiene il nome di dominio del client RDC.</span><span class="sxs-lookup"><span data-stu-id="a2206-111">A pointer to a **BSTR** variable that contains the domain name of the RDC client.</span></span> <span data-ttu-id="a2206-112">Al termine dell'utilizzo della stringa, liberarla chiamando la funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="a2206-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2206-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2206-113">Requirements</span></span>



| <span data-ttu-id="a2206-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2206-114">Requirement</span></span> | <span data-ttu-id="a2206-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a2206-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2206-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2206-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a2206-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a2206-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="a2206-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2206-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a2206-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2206-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="a2206-120">IDL</span><span class="sxs-lookup"><span data-stu-id="a2206-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2206-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2206-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2206-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2206-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2206-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a2206-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

