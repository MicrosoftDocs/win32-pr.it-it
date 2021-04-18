---
title: Struttura MCI_SAVE_PARMS (Mciapi. h)
description: La \_ \_ struttura di salvataggio parametri MCI contiene le informazioni sul nome del file per il \_ comando di salvataggio MCI.
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- Struttura MCI_SAVE_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301172"
---
# <a name="mci_save_parms-structure"></a><span data-ttu-id="9ea9b-104">\_Struttura Salva \_ parametri di MCI</span><span class="sxs-lookup"><span data-stu-id="9ea9b-104">MCI\_SAVE\_PARMS structure</span></span>

<span data-ttu-id="9ea9b-105">La struttura di **\_ salvataggio \_ parametri MCI** contiene le informazioni sul nome del file per il comando di [**\_ salvataggio MCI**](mci-save.md) .</span><span class="sxs-lookup"><span data-stu-id="9ea9b-105">The **MCI\_SAVE\_PARMS** structure contains the filename information for the [**MCI\_SAVE**](mci-save.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ea9b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ea9b-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a><span data-ttu-id="9ea9b-107">Members</span><span class="sxs-lookup"><span data-stu-id="9ea9b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ea9b-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="9ea9b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="9ea9b-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="9ea9b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="9ea9b-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="9ea9b-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="9ea9b-111">Nome del file da salvare.</span><span class="sxs-lookup"><span data-stu-id="9ea9b-111">Name of file to save.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ea9b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ea9b-112">Remarks</span></span>

<span data-ttu-id="9ea9b-113">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="9ea9b-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ea9b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ea9b-114">Requirements</span></span>



| <span data-ttu-id="9ea9b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ea9b-115">Requirement</span></span> | <span data-ttu-id="9ea9b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea9b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea9b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ea9b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9ea9b-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ea9b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9ea9b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ea9b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9ea9b-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ea9b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9ea9b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ea9b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ea9b-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ea9b-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ea9b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ea9b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea9b-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="9ea9b-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9ea9b-125">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="9ea9b-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="9ea9b-126">**salvataggio di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="9ea9b-126">**MCI\_SAVE**</span></span>](mci-save.md)
</dt> <dt>

<span data-ttu-id="9ea9b-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ea9b-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

