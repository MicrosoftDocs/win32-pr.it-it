---
description: 'Versione utilizzabile del metodo IMFPMPHost:: CreateObjectByCLSID.'
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: RemoteCreateObjectByCLSID (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e57307ece851484675d01a699037647efad771d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308480"
---
# <a name="remotecreateobjectbyclsid"></a><span data-ttu-id="2c2bd-103">RemoteCreateObjectByCLSID</span><span class="sxs-lookup"><span data-stu-id="2c2bd-103">RemoteCreateObjectByCLSID</span></span>

<span data-ttu-id="2c2bd-104">Versione utilizzabile del metodo [**IMFPMPHost:: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) .</span><span class="sxs-lookup"><span data-stu-id="2c2bd-104">Remotable version of the [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) method.</span></span>

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a><span data-ttu-id="2c2bd-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c2bd-105">Remarks</span></span>

<span data-ttu-id="2c2bd-106">Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="2c2bd-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="2c2bd-107">Il metodo non viene visualizzato in vtable per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2c2bd-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="2c2bd-108">Se [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.</span><span class="sxs-lookup"><span data-stu-id="2c2bd-108">If [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c2bd-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c2bd-109">Requirements</span></span>



| <span data-ttu-id="2c2bd-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c2bd-110">Requirement</span></span> | <span data-ttu-id="2c2bd-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2c2bd-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2bd-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c2bd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2c2bd-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c2bd-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c2bd-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c2bd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2c2bd-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c2bd-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c2bd-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c2bd-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c2bd-117"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c2bd-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="2c2bd-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="2c2bd-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c2bd-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c2bd-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="2c2bd-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c2bd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c2bd-121">**IMFPMPHost**</span><span class="sxs-lookup"><span data-stu-id="2c2bd-121">**IMFPMPHost**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[<span data-ttu-id="2c2bd-122">Sessione multimediale PMP</span><span class="sxs-lookup"><span data-stu-id="2c2bd-122">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="2c2bd-123">Percorso supporto protetto</span><span class="sxs-lookup"><span data-stu-id="2c2bd-123">Protected Media Path</span></span>](protected-media-path.md)
</dt> </dl>

 

 




