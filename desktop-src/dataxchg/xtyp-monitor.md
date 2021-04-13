---
title: Transazione XTYP_MONITOR (DDEML. h)
description: Una funzione di callback DDE del debugger Dynamic Data Exchange (DDE), DdeCallback, riceve la \_ transazione di monitoraggio XTYP ogni volta che si verifica un evento DDE nel sistema.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- Scambio di dati delle transazioni XTYP_MONITOR
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400512"
---
# <a name="xtyp_monitor-transaction"></a><span data-ttu-id="f1eeb-104">\_Transazione monitoraggio XTYP</span><span class="sxs-lookup"><span data-stu-id="f1eeb-104">XTYP\_MONITOR transaction</span></span>

<span data-ttu-id="f1eeb-105">Una funzione di callback DDE del debugger Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione di **\_ monitoraggio XTYP** ogni volta che si verifica un evento DDE nel sistema.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-105">A Dynamic Data Exchange (DDE) debugger's DDE callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_MONITOR** transaction whenever a DDE event occurs in the system.</span></span> <span data-ttu-id="f1eeb-106">Per ricevere questa transazione, un'applicazione deve specificare il valore di **\_ monitoraggio APPCLASS** quando chiama la funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="f1eeb-106">To receive this transaction, an application must specify the **APPCLASS\_MONITOR** value when it calls the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="f1eeb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1eeb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1eeb-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="f1eeb-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="f1eeb-109">Tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="f1eeb-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="f1eeb-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f1eeb-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1eeb-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="f1eeb-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="f1eeb-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1eeb-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="f1eeb-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="f1eeb-115">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1eeb-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="f1eeb-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="f1eeb-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1eeb-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="f1eeb-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="f1eeb-119">Handle per un oggetto DDE che contiene informazioni sull'evento DDE.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-119">A handle to a DDE object that contains information about the DDE event.</span></span> <span data-ttu-id="f1eeb-120">L'applicazione deve usare la funzione [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) per ottenere un puntatore all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-120">The application should use the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function to obtain a pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="f1eeb-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="f1eeb-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="f1eeb-122">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1eeb-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="f1eeb-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="f1eeb-124">Evento DDE.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-124">The DDE event.</span></span> <span data-ttu-id="f1eeb-125">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f1eeb-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f1eeb-126">Value</span></span>                                                                                                                                                                                                                      | <span data-ttu-id="f1eeb-127">Significato</span><span class="sxs-lookup"><span data-stu-id="f1eeb-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <span data-ttu-id="f1eeb-128"><dt>**MF \_ CALLBACK**</dt> <dt>0x08000000</dt></span><span class="sxs-lookup"><span data-stu-id="f1eeb-128"><dt>**MF\_CALLBACKS**</dt> <dt>0x08000000</dt></span></span> </dl> | <span data-ttu-id="f1eeb-129">Il sistema ha inviato una transazione a una funzione di callback DDE.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-129">The system sent a transaction to a DDE callback function.</span></span> <span data-ttu-id="f1eeb-130">L'oggetto DDE contiene una struttura [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) che fornisce informazioni sulla transazione.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-130">The DDE object contains a [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) structure that provides information about the transaction.</span></span><br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <span data-ttu-id="f1eeb-131"><dt>**MF \_**</dt> <dt>0x40000000</dt> Conv</span><span class="sxs-lookup"><span data-stu-id="f1eeb-131"><dt>**MF\_CONV**</dt> <dt>0x40000000</dt></span></span> </dl>                | <span data-ttu-id="f1eeb-132">Una conversazione DDE è stata stabilita o terminata.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-132">A DDE conversation was established or terminated.</span></span> <span data-ttu-id="f1eeb-133">L'oggetto DDE contiene una struttura [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) che fornisce informazioni sulla conversazione.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-133">The DDE object contains a [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) structure that provides information about the conversation.</span></span><br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <span data-ttu-id="f1eeb-134"><dt>**MF \_ ERRORI**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="f1eeb-134"><dt>**MF\_ERRORS**</dt> <dt>0x10000000</dt></span></span> </dl>          | <span data-ttu-id="f1eeb-135">Si è verificato un errore DDE.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-135">A DDE error occurred.</span></span> <span data-ttu-id="f1eeb-136">L'oggetto DDE contiene una struttura [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) che fornisce informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-136">The DDE object contains a [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) structure that provides information about the error.</span></span><br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <span data-ttu-id="f1eeb-137"><dt>**MF \_ HSZ \_ info**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="f1eeb-137"><dt>**MF\_HSZ\_INFO**</dt> <dt>0x01000000</dt></span></span> </dl>   | <span data-ttu-id="f1eeb-138">Un'applicazione DDE ha creato, rilasciato o incrementato il conteggio di utilizzo di un handle di stringa oppure è stato liberato un handle di stringa come risultato di una chiamata alla funzione [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="f1eeb-138">A DDE application created, freed, or incremented the usage count of a string handle, or a string handle was freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> <span data-ttu-id="f1eeb-139">L'oggetto DDE contiene una struttura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) che fornisce informazioni sull'handle di stringa.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-139">The DDE object contains a [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure that provides information about the string handle.</span></span><br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <span data-ttu-id="f1eeb-140"><dt>**MF \_ COLLEGAMENTI**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="f1eeb-140"><dt>**MF\_LINKS**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="f1eeb-141">Un'applicazione DDE ha avviato o arrestato un ciclo di notifica.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-141">A DDE application started or stopped an advise loop.</span></span> <span data-ttu-id="f1eeb-142">L'oggetto DDE contiene una struttura [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) che fornisce informazioni sul ciclo di notifica.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-142">The DDE object contains a [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) structure that provides information about the advise loop.</span></span><br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <span data-ttu-id="f1eeb-143"><dt>**MF \_**</dt> <dt>0x04000000</dt> POSTMSGS</span><span class="sxs-lookup"><span data-stu-id="f1eeb-143"><dt>**MF\_POSTMSGS**</dt> <dt>0x04000000</dt></span></span> </dl>    | <span data-ttu-id="f1eeb-144">Il sistema o un'applicazione ha inviato un messaggio DDE.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-144">The system or an application posted a DDE message.</span></span> <span data-ttu-id="f1eeb-145">L'oggetto DDE contiene una struttura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) che fornisce informazioni sul messaggio.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-145">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <span data-ttu-id="f1eeb-146"><dt>**MF \_**</dt> <dt>0x02000000</dt> SENDMSGS</span><span class="sxs-lookup"><span data-stu-id="f1eeb-146"><dt>**MF\_SENDMSGS**</dt> <dt>0x02000000</dt></span></span> </dl>    | <span data-ttu-id="f1eeb-147">Il sistema o un'applicazione ha inviato un messaggio DDE.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-147">The system or an application sent a DDE message.</span></span> <span data-ttu-id="f1eeb-148">L'oggetto DDE contiene una struttura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) che fornisce informazioni sul messaggio.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-148">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1eeb-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1eeb-149">Return value</span></span>

<span data-ttu-id="f1eeb-150">Se la funzione di callback elabora questa transazione, deve restituire 0.</span><span class="sxs-lookup"><span data-stu-id="f1eeb-150">If the callback function processes this transaction, it should return 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1eeb-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1eeb-151">Requirements</span></span>



| <span data-ttu-id="f1eeb-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1eeb-152">Requirement</span></span> | <span data-ttu-id="f1eeb-153">Valore</span><span class="sxs-lookup"><span data-stu-id="f1eeb-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1eeb-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1eeb-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f1eeb-155">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1eeb-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f1eeb-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1eeb-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f1eeb-157">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1eeb-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f1eeb-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1eeb-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1eeb-159"><dt>DDEML. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1eeb-159"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1eeb-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1eeb-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1eeb-161">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f1eeb-162">**DdeAccessData**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-162">**DdeAccessData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[<span data-ttu-id="f1eeb-163">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-163">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="f1eeb-164">**DdeUninitialize**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-164">**DdeUninitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[<span data-ttu-id="f1eeb-165">**MONCBSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-165">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[<span data-ttu-id="f1eeb-166">**MONCONVSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-166">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[<span data-ttu-id="f1eeb-167">**MONERRSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-167">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[<span data-ttu-id="f1eeb-168">**MONHSZSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-168">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[<span data-ttu-id="f1eeb-169">**MONLINKSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-169">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[<span data-ttu-id="f1eeb-170">**MONMSGSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-170">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

<span data-ttu-id="f1eeb-171">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f1eeb-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f1eeb-172">Libreria di gestione Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="f1eeb-172">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

