---
title: Proprietà nome utente ITsSbClientConnection
description: Recupera un valore che indica il nome dell'utente che ha avviato la connessione.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- Proprietà UserName Servizi Desktop remoto
- Servizi Desktop remoto proprietà UserName, interfaccia ITsSbClientConnection
- Interfaccia ITsSbClientConnection Servizi Desktop remoto, proprietà UserName
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bd3c1e5bb588ffb276b336cd945f32a0c19afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341143"
---
# <a name="itssbclientconnectionusername-property"></a><span data-ttu-id="e2144-106">Proprietà ITsSbClientConnection:: UserName</span><span class="sxs-lookup"><span data-stu-id="e2144-106">ITsSbClientConnection::UserName property</span></span>

<span data-ttu-id="e2144-107">Recupera un valore che indica il nome dell'utente che ha avviato la connessione.</span><span class="sxs-lookup"><span data-stu-id="e2144-107">Retrieves a value that indicates the name of the user who initiated the connection.</span></span>

<span data-ttu-id="e2144-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e2144-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2144-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2144-109">Syntax</span></span>


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="e2144-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e2144-110">Property value</span></span>

<span data-ttu-id="e2144-111">Puntatore a un nome utente.</span><span class="sxs-lookup"><span data-stu-id="e2144-111">A pointer to a user name.</span></span> <span data-ttu-id="e2144-112">Al termine dell'utilizzo della stringa, liberarla chiamando la funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="e2144-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2144-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2144-113">Requirements</span></span>



| <span data-ttu-id="e2144-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2144-114">Requirement</span></span> | <span data-ttu-id="e2144-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e2144-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2144-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2144-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2144-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e2144-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e2144-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2144-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2144-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e2144-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e2144-120">IDL</span><span class="sxs-lookup"><span data-stu-id="e2144-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2144-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2144-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2144-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2144-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2144-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="e2144-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

