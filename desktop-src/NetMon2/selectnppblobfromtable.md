---
description: La funzione SelectNPPBlobFromTable seleziona una scheda di interfaccia di rete da una tabella BLOB NPP specificata.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Funzione SelectNPPBlobFromTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226252"
---
# <a name="selectnppblobfromtable-function"></a><span data-ttu-id="9ad85-103">SelectNPPBlobFromTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="9ad85-103">SelectNPPBlobFromTable function</span></span>

<span data-ttu-id="9ad85-104">La funzione **SelectNPPBlobFromTable** seleziona una scheda di interfaccia di rete da una tabella BLOB NPP specificata.</span><span class="sxs-lookup"><span data-stu-id="9ad85-104">The **SelectNPPBlobFromTable** function selects a NIC from a supplied NPP BLOB table.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad85-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ad85-105">Syntax</span></span>


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="9ad85-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ad85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ad85-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ad85-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ad85-108">Handle per la finestra che visualizza la finestra di dialogo **Seleziona rete** .</span><span class="sxs-lookup"><span data-stu-id="9ad85-108">Handle to the window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9ad85-109">*pBlobTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ad85-109">*pBlobTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ad85-110">Puntatore alla tabella BLOB fornita.</span><span class="sxs-lookup"><span data-stu-id="9ad85-110">Pointer to the supplied BLOB table.</span></span> <span data-ttu-id="9ad85-111">Network Monitor usa questa tabella per popolare la finestra di dialogo **Seleziona una rete** .</span><span class="sxs-lookup"><span data-stu-id="9ad85-111">Network Monitor uses this table to populate the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9ad85-112">*hBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9ad85-112">*hBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ad85-113">Handle per il BLOB che rappresenta la scheda di interfaccia di rete selezionata.</span><span class="sxs-lookup"><span data-stu-id="9ad85-113">Handle to the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ad85-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ad85-114">Return value</span></span>

<span data-ttu-id="9ad85-115">Se la funzione ha esito positivo e l'utente seleziona una scheda di interfaccia di rete, il valore restituito è NMERR \_ Success; il BLOB a cui punta *hBlob* viene compilato.</span><span class="sxs-lookup"><span data-stu-id="9ad85-115">If the function is successful and the user selects a NIC, the return value is NMERR\_SUCCESS; the BLOB pointed to by *hBlob* is filled in.</span></span>

<span data-ttu-id="9ad85-116">Se l'utente non seleziona una scheda di interfaccia di rete, il valore restituito è NMERR non è stato \_ \_ selezionato alcun NPP \_ .</span><span class="sxs-lookup"><span data-stu-id="9ad85-116">If the user does not select a NIC, the return value is NMERR\_NO\_NPP\_SELECTED.</span></span>

<span data-ttu-id="9ad85-117">Se la funzione ha esito negativo, il valore restituito è un altro valore NMERR.</span><span class="sxs-lookup"><span data-stu-id="9ad85-117">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ad85-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ad85-118">Remarks</span></span>

<span data-ttu-id="9ad85-119">Quando viene chiamato, Network Monitor Visualizza la finestra di dialogo **Seleziona rete** che può essere usata per selezionare una scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="9ad85-119">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="9ad85-120">Il BLOB di NPP che rappresenta la scheda di interfaccia di rete selezionata torna all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="9ad85-120">The NPP BLOB that represents the selected NIC returns to the calling application.</span></span>

<span data-ttu-id="9ad85-121">Per informazioni sui vari modi in cui è possibile selezionare NIC, vedere [selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md)</span><span class="sxs-lookup"><span data-stu-id="9ad85-121">To learn the various ways you can select NICs, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="9ad85-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ad85-122">Requirements</span></span>



| <span data-ttu-id="9ad85-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ad85-123">Requirement</span></span> | <span data-ttu-id="9ad85-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9ad85-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad85-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ad85-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad85-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ad85-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9ad85-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ad85-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad85-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ad85-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ad85-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ad85-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ad85-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ad85-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="9ad85-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ad85-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ad85-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ad85-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ad85-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9ad85-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ad85-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ad85-134"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ad85-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ad85-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad85-136">GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="9ad85-136">GetNPPBlobFromUI</span></span>](getnppblobfromui.md)
</dt> <dt>

[<span data-ttu-id="9ad85-137">GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="9ad85-137">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="9ad85-138">Voci BLOB speciali</span><span class="sxs-lookup"><span data-stu-id="9ad85-138">Special BLOB Entries</span></span>](special-blob-entries.md)
</dt> </dl>

 

 




