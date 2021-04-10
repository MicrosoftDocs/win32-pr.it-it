---
title: Metodi di proprietà IADsPrintQueueOperations (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsPrintQueueOperations leggono e scrivono le proprietà elencate nell'elenco seguente. Per ulteriori informazioni sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPrintQueueOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8af7aef94dd9453af690f0c5d83b1e978d3b058
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964656"
---
# <a name="iadsprintqueueoperations-property-methods"></a><span data-ttu-id="5bec6-105">Metodi di proprietà IADsPrintQueueOperations</span><span class="sxs-lookup"><span data-stu-id="5bec6-105">IADsPrintQueueOperations Property Methods</span></span>

<span data-ttu-id="5bec6-106">I metodi di proprietà dell'interfaccia [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) leggono e scrivono le proprietà elencate nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="5bec6-106">The property methods of the [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) interface read and write the properties listed in the following list.</span></span> <span data-ttu-id="5bec6-107">Per ulteriori informazioni sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5bec6-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5bec6-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5bec6-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5bec6-109">**Status**</span><span class="sxs-lookup"><span data-stu-id="5bec6-109">**Status**</span></span>
<span data-ttu-id="5bec6-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5bec6-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5bec6-111">Stato corrente delle operazioni della coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="5bec6-111">Current status of the print queue operations.</span></span> <span data-ttu-id="5bec6-112">I valori del codice di stato validi sono elencati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="5bec6-112">The valid status code values are listed in the following list.</span></span>

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

<span data-ttu-id="5bec6-113">**Annunci \_ STAMPANTE \_ sospesa** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="5bec6-113">**ADS\_PRINTER\_PAUSED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

<span data-ttu-id="5bec6-114">**Annunci \_ \_ \_ Eliminazione della stampante in sospeso** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="5bec6-114">**ADS\_PRINTER\_PENDING\_DELETION** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

<span data-ttu-id="5bec6-115">**Annunci \_ \_Errore della stampante** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="5bec6-115">**ADS\_PRINTER\_ERROR** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

<span data-ttu-id="5bec6-116">**Annunci \_ 0x00000004 (PRINTER \_ paper \_ Jam** )</span><span class="sxs-lookup"><span data-stu-id="5bec6-116">**ADS\_PRINTER\_PAPER\_JAM** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

<span data-ttu-id="5bec6-117">**Annunci \_ \_Carta \_ stampata** (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="5bec6-117">**ADS\_PRINTER\_PAPER\_OUT** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

<span data-ttu-id="5bec6-118">**Annunci \_ \_ \_ Feed manuale della stampante** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="5bec6-118">**ADS\_PRINTER\_MANUAL\_FEED** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

<span data-ttu-id="5bec6-119">**Annunci \_ \_ \_ Problema relativo alla carta della stampante** (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="5bec6-119">**ADS\_PRINTER\_PAPER\_PROBLEM** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

<span data-ttu-id="5bec6-120">**Annunci \_ STAMPANTE \_ offline** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="5bec6-120">**ADS\_PRINTER\_OFFLINE** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

<span data-ttu-id="5bec6-121">**Annunci \_ \_Io stampante \_ attivo** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="5bec6-121">**ADS\_PRINTER\_IO\_ACTIVE** (0x00000100)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

<span data-ttu-id="5bec6-122">**Annunci \_ STAMPANTE \_ occupata** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="5bec6-122">**ADS\_PRINTER\_BUSY** (0x00000200)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

<span data-ttu-id="5bec6-123">**Annunci \_ \_Stampa stampante** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="5bec6-123">**ADS\_PRINTER\_PRINTING** (0x00000400)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

<span data-ttu-id="5bec6-124">**Annunci \_ Contenitore di output della stampante \_ \_ \_ completo** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="5bec6-124">**ADS\_PRINTER\_OUTPUT\_BIN\_FULL** (0x00000800)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

<span data-ttu-id="5bec6-125">**Annunci \_ STAMPANTE \_ non \_ disponibile** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-125">**ADS\_PRINTER\_NOT\_AVAILABLE** (0x00001000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

<span data-ttu-id="5bec6-126">**Annunci \_ \_Attesa stampanti** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-126">**ADS\_PRINTER\_WAITING** (0x00002000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

<span data-ttu-id="5bec6-127">**Annunci \_ \_Elaborazione stampanti** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-127">**ADS\_PRINTER\_PROCESSING** (0x00004000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

<span data-ttu-id="5bec6-128">**Annunci \_ \_Inizializzazione stampanti** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-128">**ADS\_PRINTER\_INITIALIZING** (0x00008000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

<span data-ttu-id="5bec6-129">**Annunci \_ \_Riscaldamento della \_ stampante** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-129">**ADS\_PRINTER\_WARMING\_UP** (0x00010000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

<span data-ttu-id="5bec6-130">**Annunci \_ \_Toner \_ di stampa basso** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-130">**ADS\_PRINTER\_TONER\_LOW** (0x00020000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

<span data-ttu-id="5bec6-131">**Annunci \_ STAMPANTE \_ senza \_ toner** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-131">**ADS\_PRINTER\_NO\_TONER** (0x00040000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

<span data-ttu-id="5bec6-132">**Annunci \_ Pagina della stampante \_ \_ Punt** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-132">**ADS\_PRINTER\_PAGE\_PUNT** (0x00080000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

<span data-ttu-id="5bec6-133">**Annunci \_ \_ \_ Intervento dell'utente della stampante** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-133">**ADS\_PRINTER\_USER\_INTERVENTION** (0x00100000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

<span data-ttu-id="5bec6-134">**Annunci \_ \_ \_ \_ Memoria insufficiente della stampante** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-134">**ADS\_PRINTER\_OUT\_OF\_MEMORY** (0x00200000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

<span data-ttu-id="5bec6-135">**Annunci \_ Sportello della stampante \_ \_ aperto** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-135">**ADS\_PRINTER\_DOOR\_OPEN** (0x00400000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

<span data-ttu-id="5bec6-136">**Annunci \_ \_Server stampanti \_ sconosciuto** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-136">**ADS\_PRINTER\_SERVER\_UNKNOWN** (0x00800000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

<span data-ttu-id="5bec6-137">**Annunci \_ \_ \_ Risparmio energia stampante** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="5bec6-137">**ADS\_PRINTER\_POWER\_SAVE** (0x01000000)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="5bec6-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5bec6-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bec6-139">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="5bec6-139">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="5bec6-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="5bec6-140">Examples</span></span>

<span data-ttu-id="5bec6-141">Nell'esempio di codice seguente Visual Basic viene verificato che una stampante sia bloccata.</span><span class="sxs-lookup"><span data-stu-id="5bec6-141">The following Visual Basic code example verifies that a printer is jammed.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



<span data-ttu-id="5bec6-142">Nell'esempio di codice C++ riportato di seguito viene verificato che una stampante sia bloccata.</span><span class="sxs-lookup"><span data-stu-id="5bec6-142">The following C++ code example verifies that a printer is jammed.</span></span>


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="5bec6-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bec6-143">Requirements</span></span>



| <span data-ttu-id="5bec6-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bec6-144">Requirement</span></span> | <span data-ttu-id="5bec6-145">Valore</span><span class="sxs-lookup"><span data-stu-id="5bec6-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bec6-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bec6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5bec6-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5bec6-147">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="5bec6-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bec6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5bec6-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bec6-149">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="5bec6-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bec6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bec6-151"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bec6-151"><dt>Iads.h</dt></span></span> </dl>           |
| <span data-ttu-id="5bec6-152">DLL</span><span class="sxs-lookup"><span data-stu-id="5bec6-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bec6-153"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bec6-153"><dt>Activeds.dll</dt></span></span> </dl>     |
| <span data-ttu-id="5bec6-154">IID</span><span class="sxs-lookup"><span data-stu-id="5bec6-154">IID</span></span><br/>                      | <span data-ttu-id="5bec6-155">IID \_ IADsPrintQueueOperations è definito come 124BE5C0-156E-11CF-A986-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="5bec6-155">IID\_IADsPrintQueueOperations is defined as 124BE5C0-156E-11CF-A986-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bec6-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bec6-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bec6-157">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="5bec6-157">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="5bec6-158">**IADsPrintQueueOperations**</span><span class="sxs-lookup"><span data-stu-id="5bec6-158">**IADsPrintQueueOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





