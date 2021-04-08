---
description: Seleziona una scheda di interfaccia di rete Register.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Funzione GetNPPBlobFromUI (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967775"
---
# <a name="getnppblobfromui-function"></a><span data-ttu-id="8f53a-103">GetNPPBlobFromUI (funzione)</span><span class="sxs-lookup"><span data-stu-id="8f53a-103">GetNPPBlobFromUI function</span></span>

<span data-ttu-id="8f53a-104">La funzione **GetNPPBlobFromUI** seleziona una scheda di interfaccia di rete Register.</span><span class="sxs-lookup"><span data-stu-id="8f53a-104">The **GetNPPBlobFromUI** function selects a register NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f53a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f53a-105">Syntax</span></span>


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="8f53a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f53a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f53a-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f53a-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f53a-108">Handle per una finestra che visualizza la finestra di dialogo **Seleziona rete** .</span><span class="sxs-lookup"><span data-stu-id="8f53a-108">A handle to a window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8f53a-109">*hFilterBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f53a-109">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f53a-110">Handle per un [*BLOB di filtro*](f.md) usato per limitare le schede di rete visualizzate.</span><span class="sxs-lookup"><span data-stu-id="8f53a-110">A handle to a [*filter BLOB*](f.md) used to limit which NICs are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="8f53a-111">*phBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8f53a-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f53a-112">Puntatore all'handle del BLOB che rappresenta la scheda di interfaccia di rete selezionata.</span><span class="sxs-lookup"><span data-stu-id="8f53a-112">A pointer to the handle of the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f53a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f53a-113">Return value</span></span>

<span data-ttu-id="8f53a-114">Se la funzione ha esito positivo (l'utente seleziona una scheda di interfaccia di rete), il valore restituito è NMERR \_ Success e il BLOB a cui punta *phBlob* viene compilato.</span><span class="sxs-lookup"><span data-stu-id="8f53a-114">If the function is successful (the user selects a NIC), the return value is NMERR\_SUCCESS, and the BLOB that *phBlob* points to is filled in.</span></span>

<span data-ttu-id="8f53a-115">Se l'utente non seleziona una scheda di interfaccia di rete, il valore restituito è **NMERR non è stato \_ \_ \_ selezionato alcun NPP**.</span><span class="sxs-lookup"><span data-stu-id="8f53a-115">If the user does not select an NIC, the return value is **NMERR\_NO\_NPP\_SELECTED**.</span></span>

<span data-ttu-id="8f53a-116">Se la funzione ha esito negativo, il valore restituito è un altro valore NMERR.</span><span class="sxs-lookup"><span data-stu-id="8f53a-116">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f53a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f53a-117">Remarks</span></span>

<span data-ttu-id="8f53a-118">Quando viene chiamato, Network Monitor Visualizza la finestra di dialogo **Seleziona rete** che può essere usata per selezionare una scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="8f53a-118">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="8f53a-119">Il BLOB di NPP che rappresenta la scheda di interfaccia di rete viene restituito all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="8f53a-119">The NPP BLOB that represents the NIC is returned to the calling application.</span></span>

<span data-ttu-id="8f53a-120">Se il BLOB denominato da *hFilterBlob* è un [*BLOB speciale*](s.md), il Finder tenterà di elaborarlo.</span><span class="sxs-lookup"><span data-stu-id="8f53a-120">If the BLOB named by *hFilterBlob* is a [*special BLOB*](s.md), the finder will attempt to process it.</span></span> <span data-ttu-id="8f53a-121">Un esempio potrebbe essere una chiamata che in precedenza aveva restituito un BLOB speciale dall'oggetto NPP remoto.</span><span class="sxs-lookup"><span data-stu-id="8f53a-121">An example would be a call that had previously returned a special BLOB from the remote NPP.</span></span> <span data-ttu-id="8f53a-122">L'applicazione ha inserito il tag richiesto, il nome del computer \_ .</span><span class="sxs-lookup"><span data-stu-id="8f53a-122">The application inserted the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="8f53a-123">In questa situazione, il Finder passa questo BLOB all'oggetto NPP remoto, che restituisce quindi una tabella di BLOB NPP che rappresenta il computer richiesto.</span><span class="sxs-lookup"><span data-stu-id="8f53a-123">In this situation, the finder would pass this BLOB to the remote NPP, which would then return a table of NPP BLOBs representing the machine requested.</span></span> <span data-ttu-id="8f53a-124">Questi BLOB di NPP remoti verranno visualizzati nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8f53a-124">These remote NPP BLOBs would appear in the dialog box.</span></span>

<span data-ttu-id="8f53a-125">Il chiamante deve chiamare la funzione [DestroyBlob](destroyblob.md) , che elimina il BLOB restituito quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="8f53a-125">The caller must call the [DestroyBlob](destroyblob.md) function, which destroys the returned BLOB when it is no longer required.</span></span>



| <span data-ttu-id="8f53a-126">Per altre informazioni su</span><span class="sxs-lookup"><span data-stu-id="8f53a-126">For more information about</span></span> | <span data-ttu-id="8f53a-127">Vedere</span><span class="sxs-lookup"><span data-stu-id="8f53a-127">See</span></span>                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8f53a-128">Tre modi per selezionare le schede di rete</span><span class="sxs-lookup"><span data-stu-id="8f53a-128">Three ways to select NICs</span></span>  | [<span data-ttu-id="8f53a-129">Selezione di una scheda di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="8f53a-129">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |
| <span data-ttu-id="8f53a-130">Specifica di un BLOB di filtro</span><span class="sxs-lookup"><span data-stu-id="8f53a-130">Specifying a filter BLOB</span></span>   | [<span data-ttu-id="8f53a-131">Specifica di un BLOB di filtro</span><span class="sxs-lookup"><span data-stu-id="8f53a-131">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a><span data-ttu-id="8f53a-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f53a-132">Requirements</span></span>



| <span data-ttu-id="8f53a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f53a-133">Requirement</span></span> | <span data-ttu-id="8f53a-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8f53a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f53a-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f53a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8f53a-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f53a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8f53a-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f53a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8f53a-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f53a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8f53a-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f53a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f53a-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f53a-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="8f53a-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="8f53a-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f53a-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f53a-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="8f53a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="8f53a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f53a-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f53a-144"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f53a-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f53a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f53a-146">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="8f53a-146">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="8f53a-147">SelectNPPBlobFromTable</span><span class="sxs-lookup"><span data-stu-id="8f53a-147">SelectNPPBlobFromTable</span></span>](selectnppblobfromtable.md)
</dt> </dl>

 

 




