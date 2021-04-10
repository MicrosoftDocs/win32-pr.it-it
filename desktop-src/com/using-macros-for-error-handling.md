---
title: Uso delle macro per la gestione degli errori
description: COM definisce diverse macro che semplificano l'utilizzo dei valori HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730423"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="ebd41-103">Uso delle macro per la gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="ebd41-103">Using Macros for Error Handling</span></span>

<span data-ttu-id="ebd41-104">COM definisce diverse macro che semplificano l'utilizzo dei valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ebd41-104">COM defines a number of macros that make it easier to work with **HRESULT** values.</span></span>

<span data-ttu-id="ebd41-105">Nella tabella seguente sono descritte le macro di gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="ebd41-105">The error handling macros are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebd41-106">Macro</span><span class="sxs-lookup"><span data-stu-id="ebd41-106">Macro</span></span></th>
<th><span data-ttu-id="ebd41-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebd41-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ebd41-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-109">Restituisce un valore <strong>HRESULT</strong> dato il bit di gravità, il codice della struttura e il codice di errore che comprendono <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebd41-109">Returns an <strong>HRESULT</strong> given the severity bit, facility code, and error code that comprise the <strong>HRESULT</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ebd41-110">La chiamata di <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> per la verifica S_OK comporta una riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ebd41-110">Calling <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> for S_OK verification carries a performance penalty.</span></span> <span data-ttu-id="ebd41-111">Per ottenere risultati ottimali, è consigliabile non utilizzare periodicamente <strong>MAKE_HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="ebd41-111">You should not routinely use <strong>MAKE_HRESULT</strong> for successful results.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebd41-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-113">Restituisce un oggetto <strong>SCODE</strong> dato il bit di gravità, il codice della struttura e il codice di errore che comprendono <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebd41-113">Returns an <strong>SCODE</strong> given the severity bit, facility code, and error code that comprise the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebd41-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-115">Estrae la parte relativa al codice di errore del valore <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebd41-115">Extracts the error code portion of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebd41-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-117">Estrae il codice di struttura del valore <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebd41-117">Extracts the facility code of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebd41-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-119">Estrae il bit di gravità del valore <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebd41-119">Extracts the severity bit of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebd41-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-121">Estrae la parte relativa al codice di errore di <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebd41-121">Extracts the error code portion of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebd41-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-123">Estrae il codice di struttura di <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebd41-123">Extracts the facility code of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebd41-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-125">Estrae il campo di gravità di <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="ebd41-125">Extracts the severity field of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebd41-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>COMPLETATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-127">Verifica il bit di gravità di <strong>SCODE</strong> o <strong>HRESULT</strong>; restituisce <strong>true</strong> se il livello di gravità è zero e <strong>false</strong> se è uno.</span><span class="sxs-lookup"><span data-stu-id="ebd41-127">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is zero and <strong>FALSE</strong> if it is one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebd41-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FALLITO</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FAILED</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-129">Verifica il bit di gravità di <strong>SCODE</strong> o <strong>HRESULT</strong>; restituisce <strong>true</strong> se il livello di gravità è uno e <strong>false</strong> se è zero.</span><span class="sxs-lookup"><span data-stu-id="ebd41-129">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is one and <strong>FALSE</strong> if it is zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebd41-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-131">Fornisce un test generico per gli errori relativi a qualsiasi valore di stato.</span><span class="sxs-lookup"><span data-stu-id="ebd41-131">Provides a generic test for errors on any status value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebd41-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-133">Esegue il mapping di un <a href="/windows/desktop/Debug/system-error-codes">codice di errore di sistema</a> a un valore <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="ebd41-133">Maps a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> to an <strong>HRESULT</strong> value.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebd41-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span><span class="sxs-lookup"><span data-stu-id="ebd41-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span></span><br/></td>
<td><span data-ttu-id="ebd41-135">Esegue il mapping di un valore di stato di NT a un valore <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="ebd41-135">Maps an NT status value to an <strong>HRESULT</strong> value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ebd41-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebd41-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebd41-137">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="ebd41-137">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

