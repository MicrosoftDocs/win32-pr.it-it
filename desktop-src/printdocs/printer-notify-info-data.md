---
description: La \_ struttura di \_ dati notifica informazioni stampante \_ identifica un campo informazioni sul processo o sulla stampante e fornisce i dati correnti per quel campo.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: Struttura PRINTER_NOTIFY_INFO_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231948"
---
# <a name="printer_notify_info_data-structure"></a><span data-ttu-id="8c6f5-103">\_ \_ \_ Struttura dei dati di notifica della stampante</span><span class="sxs-lookup"><span data-stu-id="8c6f5-103">PRINTER\_NOTIFY\_INFO\_DATA structure</span></span>

<span data-ttu-id="8c6f5-104">La struttura di **\_ \_ \_ dati notifica informazioni stampante** identifica un campo informazioni sul processo o sulla stampante e fornisce i dati correnti per quel campo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-104">The **PRINTER\_NOTIFY\_INFO\_DATA** structure identifies a job or printer information field and provides the current data for that field.</span></span>

<span data-ttu-id="8c6f5-105">La funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) restituisce una struttura di [**\_ \_ informazioni di notifica della stampante**](printer-notify-info.md) , che contiene una matrice di strutture di **\_ \_ \_ dati di notifica della stampante** .</span><span class="sxs-lookup"><span data-stu-id="8c6f5-105">The [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function returns a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of **PRINTER\_NOTIFY\_INFO\_DATA** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c6f5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c6f5-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a><span data-ttu-id="8c6f5-107">Members</span><span class="sxs-lookup"><span data-stu-id="8c6f5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c6f5-108">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="8c6f5-109">Indica il tipo di informazioni fornite.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-109">Indicates the type of information provided.</span></span> <span data-ttu-id="8c6f5-110">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="8c6f5-111">Valore</span><span class="sxs-lookup"><span data-stu-id="8c6f5-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="8c6f5-112">Significato</span><span class="sxs-lookup"><span data-stu-id="8c6f5-112">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="8c6f5-113"><dt>**Processo \_ di Invia notifica al \_ tipo**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="8c6f5-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="8c6f5-114">Indica che il membro del **campo** specifica una \_ costante di campo Notify di processo \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="8c6f5-114">Indicates that the **Field** member specifies a JOB\_NOTIFY\_FIELD\_\* constant.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="8c6f5-115"><dt>**Stampante \_ NOTIFICA \_ tipo**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="8c6f5-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="8c6f5-116">Indica che il membro del **campo** specifica una \_ costante di campo Notify della stampante \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="8c6f5-116">Indicates that the **Field** member specifies a PRINTER\_NOTIFY\_FIELD\_\* constant.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8c6f5-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-117">**Field**</span></span>
</dt> <dd>

<span data-ttu-id="8c6f5-118">Indica il campo modificato.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-118">Indicates the field that changed.</span></span> <span data-ttu-id="8c6f5-119">Per un elenco di valori possibili, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-119">For a list of possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="8c6f5-120">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-120">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="8c6f5-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8c6f5-122">**Id**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-122">**Id**</span></span>
</dt> <dd>

<span data-ttu-id="8c6f5-123">Indica l'identificatore del processo se il membro del **tipo** specifica il tipo di notifica del processo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8c6f5-123">Indicates the job identifier if the **Type** member specifies JOB\_NOTIFY\_TYPE.</span></span> <span data-ttu-id="8c6f5-124">Se il membro del **tipo** specifica il \_ tipo di notifica della stampante \_ , questo membro non è definito.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-124">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="8c6f5-125">**NotifyData**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-125">**NotifyData**</span></span>
</dt> <dd>

<span data-ttu-id="8c6f5-126">Unione di informazioni sui dati basate sui membri del **tipo** e del **campo** .</span><span class="sxs-lookup"><span data-stu-id="8c6f5-126">A union of data information based on the **Type** and **Field** members.</span></span> <span data-ttu-id="8c6f5-127">Per una descrizione del tipo di dati associato a ogni campo, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-127">For a description of the type of data associated with each field, see the Remarks section.</span></span>

<dl> <dt>

<span data-ttu-id="8c6f5-128">**adwData \[ 2\]**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-128">**adwData\[2\]**</span></span>
</dt> <dd>

<span data-ttu-id="8c6f5-129">Matrice di due valori **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8c6f5-129">An array of two **DWORD** values.</span></span> <span data-ttu-id="8c6f5-130">Per i campi di informazioni che usano solo un singolo **valore DWORD**, i dati sono in **adwData** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="8c6f5-130">For information fields that use only a single **DWORD**, the data is in **adwData** \[0\].</span></span>

</dd> <dt>

<span data-ttu-id="8c6f5-131">**Dati**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-131">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c6f5-132">**cbBuf**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-132">**cbBuf**</span></span>
</dt> <dd>

<span data-ttu-id="8c6f5-133">Indica la dimensione, in byte, del buffer a cui punta **pbuf**.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-133">Indicates the size, in bytes, of the buffer pointed to by **pBuf**.</span></span>

</dd> <dt>

<span data-ttu-id="8c6f5-134">**pBuf**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-134">**pBuf**</span></span>
</dt> <dd>

<span data-ttu-id="8c6f5-135">Puntatore a un buffer che contiene i dati correnti del campo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-135">Pointer to a buffer that contains the field's current data.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c6f5-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c6f5-136">Remarks</span></span>

<span data-ttu-id="8c6f5-137">Se il membro del **tipo** specifica il \_ tipo di notifica della stampante \_ , il membro del **campo** può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-137">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8c6f5-138">Campo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-138">Field</span></span></th>
<th><span data-ttu-id="8c6f5-139">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8c6f5-139">Type of data</span></span></th>
<th><span data-ttu-id="8c6f5-140">Valore</span><span class="sxs-lookup"><span data-stu-id="8c6f5-140">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c6f5-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="8c6f5-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span></span></td>
<td><span data-ttu-id="8c6f5-142">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-142">Not supported.</span></span></td>
<td><span data-ttu-id="8c6f5-143">0x00</span><span class="sxs-lookup"><span data-stu-id="8c6f5-143">0x00</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span><span class="sxs-lookup"><span data-stu-id="8c6f5-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span></span></td>
<td><span data-ttu-id="8c6f5-145"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene il nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-145"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer.</span></span></td>
<td><span data-ttu-id="8c6f5-146">0x01</span><span class="sxs-lookup"><span data-stu-id="8c6f5-146">0x01</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span><span class="sxs-lookup"><span data-stu-id="8c6f5-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span></span></td>
<td><span data-ttu-id="8c6f5-148"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che identifica il punto di condivisione per la stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-148"><strong>pBuf</strong> is a pointer to a null-terminated string that identifies the share point for the printer.</span></span></td>
<td><span data-ttu-id="8c6f5-149">0x02</span><span class="sxs-lookup"><span data-stu-id="8c6f5-149">0x02</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span><span class="sxs-lookup"><span data-stu-id="8c6f5-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span></span></td>
<td><span data-ttu-id="8c6f5-151"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene il nome della porta in cui verranno stampati i processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-151"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the port that the print jobs will be printed to.</span></span> <span data-ttu-id="8c6f5-152">Se &quot; &quot; si seleziona pool di stampanti, si tratta di un elenco delimitato da virgole di porte.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-152">If &quot;Printer Pooling&quot; is selected, this is a comma separated list of ports.</span></span></td>
<td><span data-ttu-id="8c6f5-153">0x03</span><span class="sxs-lookup"><span data-stu-id="8c6f5-153">0x03</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span><span class="sxs-lookup"><span data-stu-id="8c6f5-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span></span></td>
<td><span data-ttu-id="8c6f5-155"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene il nome del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-155"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer's driver.</span></span></td>
<td><span data-ttu-id="8c6f5-156">0x04</span><span class="sxs-lookup"><span data-stu-id="8c6f5-156">0x04</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-157">PRINTER_NOTIFY_FIELD_COMMENT</span><span class="sxs-lookup"><span data-stu-id="8c6f5-157">PRINTER_NOTIFY_FIELD_COMMENT</span></span></td>
<td><span data-ttu-id="8c6f5-158"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene la nuova stringa di commento, che in genere è una breve descrizione della stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-158"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new comment string, which is typically a brief description of the printer.</span></span></td>
<td><span data-ttu-id="8c6f5-159">0x05</span><span class="sxs-lookup"><span data-stu-id="8c6f5-159">0x05</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-160">PRINTER_NOTIFY_FIELD_LOCATION</span><span class="sxs-lookup"><span data-stu-id="8c6f5-160">PRINTER_NOTIFY_FIELD_LOCATION</span></span></td>
<td><span data-ttu-id="8c6f5-161"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene la nuova posizione fisica della stampante, ad esempio &quot; Bldg.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-161"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new physical location of the printer (for example, &quot;Bldg.</span></span> <span data-ttu-id="8c6f5-162">38, stanza 1164 &quot; ).</span><span class="sxs-lookup"><span data-stu-id="8c6f5-162">38, Room 1164&quot;).</span></span></td>
<td><span data-ttu-id="8c6f5-163">0x06</span><span class="sxs-lookup"><span data-stu-id="8c6f5-163">0x06</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-164">PRINTER_NOTIFY_FIELD_DEVMODE</span><span class="sxs-lookup"><span data-stu-id="8c6f5-164">PRINTER_NOTIFY_FIELD_DEVMODE</span></span></td>
<td><span data-ttu-id="8c6f5-165"><strong>pbuf</strong> è un puntatore a una struttura <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> che definisce i dati predefiniti della stampante, ad esempio l'orientamento della carta e la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-165"><strong>pBuf</strong> is a pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> structure that defines default printer data such as the paper orientation and the resolution.</span></span></td>
<td><span data-ttu-id="8c6f5-166">0x07</span><span class="sxs-lookup"><span data-stu-id="8c6f5-166">0x07</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-167">PRINTER_NOTIFY_FIELD_SEPFILE</span><span class="sxs-lookup"><span data-stu-id="8c6f5-167">PRINTER_NOTIFY_FIELD_SEPFILE</span></span></td>
<td><span data-ttu-id="8c6f5-168"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che specifica il nome del file utilizzato per creare la pagina separatore.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-168"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="8c6f5-169">Questa pagina viene utilizzata per separare i processi di stampa inviati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-169">This page is used to separate print jobs sent to the printer.</span></span></td>
<td><span data-ttu-id="8c6f5-170">0x08</span><span class="sxs-lookup"><span data-stu-id="8c6f5-170">0x08</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="8c6f5-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span></span></td>
<td><span data-ttu-id="8c6f5-172"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che specifica il nome del processore di stampa utilizzato dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-172"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span></td>
<td><span data-ttu-id="8c6f5-173">0x09</span><span class="sxs-lookup"><span data-stu-id="8c6f5-173">0x09</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c6f5-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span></span></td>
<td><span data-ttu-id="8c6f5-175"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che specifica i parametri predefiniti del processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-175"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the default print-processor parameters.</span></span></td>
<td><span data-ttu-id="8c6f5-176">0x0A</span><span class="sxs-lookup"><span data-stu-id="8c6f5-176">0x0A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-177">PRINTER_NOTIFY_FIELD_DATATYPE</span><span class="sxs-lookup"><span data-stu-id="8c6f5-177">PRINTER_NOTIFY_FIELD_DATATYPE</span></span></td>
<td><span data-ttu-id="8c6f5-178"><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzato per registrare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-178"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the data type used to record the print job.</span></span></td>
<td><span data-ttu-id="8c6f5-179">0x0B</span><span class="sxs-lookup"><span data-stu-id="8c6f5-179">0x0B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="8c6f5-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span></span></td>
<td><span data-ttu-id="8c6f5-181"><strong>pbuf</strong> è un puntatore a una struttura <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> per la stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-181"><strong>pBuf</strong> is a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> structure for the printer.</span></span> <span data-ttu-id="8c6f5-182">Il puntatore può essere <strong>null</strong> se non è presente alcun descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-182">The pointer may be <strong>NULL</strong> if there is no security descriptor.</span></span></td>
<td><span data-ttu-id="8c6f5-183">0x0C</span><span class="sxs-lookup"><span data-stu-id="8c6f5-183">0x0C</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="8c6f5-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span></span></td>
<td><span data-ttu-id="8c6f5-185"><strong>adwData</strong> [0] specifica gli attributi della stampante. i possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c6f5-185"><strong>adwData</strong> [0] specifies the printer attributes, which can be one of the following values:</span></span><dl> <span data-ttu-id="8c6f5-186">PRINTER_ATTRIBUTE_QUEUED</span><span class="sxs-lookup"><span data-stu-id="8c6f5-186">PRINTER_ATTRIBUTE_QUEUED</span></span><br />
<span data-ttu-id="8c6f5-187">PRINTER_ATTRIBUTE_DIRECT</span><span class="sxs-lookup"><span data-stu-id="8c6f5-187">PRINTER_ATTRIBUTE_DIRECT</span></span><br />
<span data-ttu-id="8c6f5-188">PRINTER_ATTRIBUTE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="8c6f5-188">PRINTER_ATTRIBUTE_DEFAULT</span></span><br />
<span data-ttu-id="8c6f5-189">PRINTER_ATTRIBUTE_SHARED</span><span class="sxs-lookup"><span data-stu-id="8c6f5-189">PRINTER_ATTRIBUTE_SHARED</span></span><br />
</dl></td>
<td><span data-ttu-id="8c6f5-190">0x0D</span><span class="sxs-lookup"><span data-stu-id="8c6f5-190">0x0D</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-191">PRINTER_NOTIFY_FIELD_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="8c6f5-191">PRINTER_NOTIFY_FIELD_PRIORITY</span></span></td>
<td><span data-ttu-id="8c6f5-192"><strong>adwData</strong> [0] specifica un valore di priorità utilizzato dallo spooler per instradare i processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-192"><strong>adwData</strong> [0] specifies a priority value that the spooler uses to route print jobs.</span></span></td>
<td><span data-ttu-id="8c6f5-193">0x0E</span><span class="sxs-lookup"><span data-stu-id="8c6f5-193">0x0E</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="8c6f5-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span></span></td>
<td><span data-ttu-id="8c6f5-195"><strong>adwData</strong> [0] specifica il valore di priorità predefinito assegnato a ogni processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-195"><strong>adwData</strong> [0] specifies the default priority value assigned to each print job.</span></span></td>
<td><span data-ttu-id="8c6f5-196">0x0F</span><span class="sxs-lookup"><span data-stu-id="8c6f5-196">0x0F</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-197">PRINTER_NOTIFY_FIELD_START_TIME</span><span class="sxs-lookup"><span data-stu-id="8c6f5-197">PRINTER_NOTIFY_FIELD_START_TIME</span></span></td>
<td><span data-ttu-id="8c6f5-198"><strong>adwData</strong> [0] specifica la prima ora di stampa di un processo da parte della stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-198"><strong>adwData</strong> [0] specifies the earliest time at which the printer will print a job.</span></span> <span data-ttu-id="8c6f5-199">(Questo valore viene specificato in minuti trascorsi dalle ore 12:00)</span><span class="sxs-lookup"><span data-stu-id="8c6f5-199">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="8c6f5-200">0x10</span><span class="sxs-lookup"><span data-stu-id="8c6f5-200">0x10</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span><span class="sxs-lookup"><span data-stu-id="8c6f5-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span></span></td>
<td><span data-ttu-id="8c6f5-202"><strong>adwData</strong> [0] specifica l'ora più recente in cui la stampante stampa un processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-202"><strong>adwData</strong> [0] specifies the latest time at which the printer will print a job.</span></span> <span data-ttu-id="8c6f5-203">(Questo valore viene specificato in minuti trascorsi dalle ore 12:00)</span><span class="sxs-lookup"><span data-stu-id="8c6f5-203">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="8c6f5-204">0x11</span><span class="sxs-lookup"><span data-stu-id="8c6f5-204">0x11</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-205">PRINTER_NOTIFY_FIELD_STATUS</span><span class="sxs-lookup"><span data-stu-id="8c6f5-205">PRINTER_NOTIFY_FIELD_STATUS</span></span></td>
<td><span data-ttu-id="8c6f5-206"><strong>adwData</strong> [0] specifica lo stato della stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-206"><strong>adwData</strong> [0] specifies the printer status.</span></span> <span data-ttu-id="8c6f5-207">Per un elenco di valori possibili, vedere la struttura <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c6f5-207">For a list of possible values, see the <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> structure.</span></span></td>
<td><span data-ttu-id="8c6f5-208">0x12</span><span class="sxs-lookup"><span data-stu-id="8c6f5-208">0x12</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span><span class="sxs-lookup"><span data-stu-id="8c6f5-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span></span></td>
<td><span data-ttu-id="8c6f5-210">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-210">Not supported.</span></span></td>
<td><span data-ttu-id="8c6f5-211">0x13</span><span class="sxs-lookup"><span data-stu-id="8c6f5-211">0x13</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-212">PRINTER_NOTIFY_FIELD_CJOBS</span><span class="sxs-lookup"><span data-stu-id="8c6f5-212">PRINTER_NOTIFY_FIELD_CJOBS</span></span></td>
<td><span data-ttu-id="8c6f5-213"><strong>adwData</strong> [0] specifica il numero di processi di stampa accodati per la stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-213"><strong>adwData</strong> [0] specifies the number of print jobs that have been queued for the printer.</span></span></td>
<td><span data-ttu-id="8c6f5-214">0x14</span><span class="sxs-lookup"><span data-stu-id="8c6f5-214">0x14</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span><span class="sxs-lookup"><span data-stu-id="8c6f5-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span></span></td>
<td><span data-ttu-id="8c6f5-216"><strong>adwData</strong> [0] specifica il numero medio di pagine al minuto stampate sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-216"><strong>adwData</strong> [0] specifies the average number of pages per minute that have been printed on the printer.</span></span></td>
<td><span data-ttu-id="8c6f5-217">0x15</span><span class="sxs-lookup"><span data-stu-id="8c6f5-217">0x15</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span><span class="sxs-lookup"><span data-stu-id="8c6f5-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span></span></td>
<td><span data-ttu-id="8c6f5-219">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-219">Not supported.</span></span></td>
<td><span data-ttu-id="8c6f5-220">0x16</span><span class="sxs-lookup"><span data-stu-id="8c6f5-220">0x16</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="8c6f5-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span></span></td>
<td><span data-ttu-id="8c6f5-222">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-222">Not supported.</span></span></td>
<td><span data-ttu-id="8c6f5-223">0x17</span><span class="sxs-lookup"><span data-stu-id="8c6f5-223">0x17</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span><span class="sxs-lookup"><span data-stu-id="8c6f5-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span></span></td>
<td><span data-ttu-id="8c6f5-225">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-225">Not supported.</span></span></td>
<td><span data-ttu-id="8c6f5-226">0x18</span><span class="sxs-lookup"><span data-stu-id="8c6f5-226">0x18</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="8c6f5-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span></span></td>
<td><span data-ttu-id="8c6f5-228">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-228">Not supported.</span></span></td>
<td><span data-ttu-id="8c6f5-229">0x19</span><span class="sxs-lookup"><span data-stu-id="8c6f5-229">0x19</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c6f5-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span><span class="sxs-lookup"><span data-stu-id="8c6f5-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span></span></td>
<td><span data-ttu-id="8c6f5-231">Questa impostazione viene impostata se il GUID dell'oggetto viene modificato.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-231">This is set if the object GUID changes.</span></span></td>
<td><span data-ttu-id="8c6f5-232">0x1A</span><span class="sxs-lookup"><span data-stu-id="8c6f5-232">0x1A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c6f5-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="8c6f5-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span></span></td>
<td><span data-ttu-id="8c6f5-234">Questa impostazione viene impostata se la connessione alla stampante viene rinominata.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-234">This is set if the printer connection is renamed.</span></span></td>
<td><span data-ttu-id="8c6f5-235">0x1B</span><span class="sxs-lookup"><span data-stu-id="8c6f5-235">0x1B</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8c6f5-236">Se il membro del **tipo** specifica il \_ tipo di notifica del processo \_ , il membro del **campo** può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-236">If the **Type** member specifies JOB\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



| <span data-ttu-id="8c6f5-237">Campo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-237">Field</span></span>                                    | <span data-ttu-id="8c6f5-238">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8c6f5-238">Type of data</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="8c6f5-239">Valore</span><span class="sxs-lookup"><span data-stu-id="8c6f5-239">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="8c6f5-240">\_ \_ \_ nome stampante campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-240">JOB\_NOTIFY\_FIELD\_PRINTER\_NAME</span></span>        | <span data-ttu-id="8c6f5-241">**pbuf** è un puntatore a una stringa con terminazione null che contiene il nome della stampante per cui viene eseguito lo spooling del processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-241">**pBuf** is a pointer to a null-terminated string containing the name of the printer for which the job is spooled.</span></span>                                                                                                                                      | <span data-ttu-id="8c6f5-242">0x00</span><span class="sxs-lookup"><span data-stu-id="8c6f5-242">0x00</span></span>  |
| <span data-ttu-id="8c6f5-243">\_ \_ \_ nome computer campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-243">JOB\_NOTIFY\_FIELD\_MACHINE\_NAME</span></span>        | <span data-ttu-id="8c6f5-244">**pbuf** è un puntatore a una stringa con terminazione null che specifica il nome del computer in cui è stato creato il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-244">**pBuf** is a pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>                                                                                                                                    | <span data-ttu-id="8c6f5-245">0x01</span><span class="sxs-lookup"><span data-stu-id="8c6f5-245">0x01</span></span>  |
| <span data-ttu-id="8c6f5-246">\_ \_ \_ nome porta campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-246">JOB\_NOTIFY\_FIELD\_PORT\_NAME</span></span>           | <span data-ttu-id="8c6f5-247">**pbuf** è un puntatore a una stringa con terminazione null che identifica la porta o le porte utilizzate per trasmettere i dati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-247">**pBuf** is a pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="8c6f5-248">Se una stampante è connessa a più di una porta, i nomi delle porte sono separati da virgole (ad esempio, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="8c6f5-248">If a printer is connected to more than one port, the names of the ports are separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span> | <span data-ttu-id="8c6f5-249">0x02</span><span class="sxs-lookup"><span data-stu-id="8c6f5-249">0x02</span></span>  |
| <span data-ttu-id="8c6f5-250">\_ \_ \_ nome utente campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-250">JOB\_NOTIFY\_FIELD\_USER\_NAME</span></span>           | <span data-ttu-id="8c6f5-251">**pbuf** è un puntatore a una stringa con terminazione null che specifica il nome dell'utente che ha inviato il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-251">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who sent the print job.</span></span>                                                                                                                                           | <span data-ttu-id="8c6f5-252">0x03</span><span class="sxs-lookup"><span data-stu-id="8c6f5-252">0x03</span></span>  |
| <span data-ttu-id="8c6f5-253">\_ \_ \_ nome notifica campo \_ notifica processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-253">JOB\_NOTIFY\_FIELD\_NOTIFY\_NAME</span></span>         | <span data-ttu-id="8c6f5-254">**pbuf** è un puntatore a una stringa con terminazione null che specifica il nome dell'utente a cui deve essere inviata una notifica quando il processo è stato stampato o quando si verifica un errore durante la stampa del processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-254">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>                                                              | <span data-ttu-id="8c6f5-255">0x04</span><span class="sxs-lookup"><span data-stu-id="8c6f5-255">0x04</span></span>  |
| <span data-ttu-id="8c6f5-256">tipo di dati del \_ campo Notify processo \_ \_</span><span class="sxs-lookup"><span data-stu-id="8c6f5-256">JOB\_NOTIFY\_FIELD\_DATATYPE</span></span>             | <span data-ttu-id="8c6f5-257">**pbuf** è un puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzati per registrare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-257">**pBuf** is a pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>                                                                                                                                         | <span data-ttu-id="8c6f5-258">0x05</span><span class="sxs-lookup"><span data-stu-id="8c6f5-258">0x05</span></span>  |
| <span data-ttu-id="8c6f5-259">\_processore di \_ \_ Stampa campo notifica processo \_</span><span class="sxs-lookup"><span data-stu-id="8c6f5-259">JOB\_NOTIFY\_FIELD\_PRINT\_PROCESSOR</span></span>     | <span data-ttu-id="8c6f5-260">**pbuf** è un puntatore a una stringa con terminazione null che specifica il nome del processore di stampa da utilizzare per stampare il processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-260">**pBuf** is a pointer to a null-terminated string that specifies the name of the print processor to be used to print the job.</span></span>                                                                                                                           | <span data-ttu-id="8c6f5-261">0x06</span><span class="sxs-lookup"><span data-stu-id="8c6f5-261">0x06</span></span>  |
| <span data-ttu-id="8c6f5-262">\_ \_ parametri Campo notifica \_ processi</span><span class="sxs-lookup"><span data-stu-id="8c6f5-262">JOB\_NOTIFY\_FIELD\_PARAMETERS</span></span>           | <span data-ttu-id="8c6f5-263">**pbuf** è un puntatore a una stringa con terminazione null che specifica i parametri del processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-263">**pBuf** is a pointer to a null-terminated string that specifies print-processor parameters.</span></span>                                                                                                                                                            | <span data-ttu-id="8c6f5-264">0x07</span><span class="sxs-lookup"><span data-stu-id="8c6f5-264">0x07</span></span>  |
| <span data-ttu-id="8c6f5-265">\_ \_ \_ nome driver campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-265">JOB\_NOTIFY\_FIELD\_DRIVER\_NAME</span></span>         | <span data-ttu-id="8c6f5-266">**pbuf** è un puntatore a una stringa con terminazione null che specifica il nome del driver della stampante da usare per elaborare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-266">**pBuf** is a pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>                                                                                                           | <span data-ttu-id="8c6f5-267">0x08</span><span class="sxs-lookup"><span data-stu-id="8c6f5-267">0x08</span></span>  |
| <span data-ttu-id="8c6f5-268">area di notifica del processo \_ \_ \_ DEVMODE</span><span class="sxs-lookup"><span data-stu-id="8c6f5-268">JOB\_NOTIFY\_FIELD\_DEVMODE</span></span>              | <span data-ttu-id="8c6f5-269">**pbuf** è un puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati dell'ambiente e dell'inizializzazione del dispositivo per il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-269">**pBuf** is a pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>                                                                                                        | <span data-ttu-id="8c6f5-270">0x09</span><span class="sxs-lookup"><span data-stu-id="8c6f5-270">0x09</span></span>  |
| <span data-ttu-id="8c6f5-271">\_ \_ stato campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-271">JOB\_NOTIFY\_FIELD\_STATUS</span></span>               | <span data-ttu-id="8c6f5-272">**adwData** \[ 0 \] specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-272">**adwData** \[0\] specifies the job status.</span></span> <span data-ttu-id="8c6f5-273">Per un elenco di valori possibili, vedere la struttura di [**informazioni sul processo \_ \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="8c6f5-273">For a list of possible values, see the [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>                                                                                                                        | <span data-ttu-id="8c6f5-274">0x0A</span><span class="sxs-lookup"><span data-stu-id="8c6f5-274">0x0A</span></span>  |
| <span data-ttu-id="8c6f5-275">\_stringa di \_ \_ stato campo notifica processo \_</span><span class="sxs-lookup"><span data-stu-id="8c6f5-275">JOB\_NOTIFY\_FIELD\_STATUS\_STRING</span></span>       | <span data-ttu-id="8c6f5-276">**pbuf** è un puntatore a una stringa con terminazione null che specifica lo stato del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-276">**pBuf** is a pointer to a null-terminated string that specifies the status of the print job.</span></span>                                                                                                                                                           | <span data-ttu-id="8c6f5-277">0x0B</span><span class="sxs-lookup"><span data-stu-id="8c6f5-277">0x0B</span></span>  |
| <span data-ttu-id="8c6f5-278">\_ \_ \_ descrittore di sicurezza campo notifica processo \_</span><span class="sxs-lookup"><span data-stu-id="8c6f5-278">JOB\_NOTIFY\_FIELD\_SECURITY\_DESCRIPTOR</span></span> | <span data-ttu-id="8c6f5-279">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-279">Not supported.</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="8c6f5-280">0x0C</span><span class="sxs-lookup"><span data-stu-id="8c6f5-280">0x0C</span></span>  |
| <span data-ttu-id="8c6f5-281">\_documento di \_ campo \_ Notify processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-281">JOB\_NOTIFY\_FIELD\_DOCUMENT</span></span>             | <span data-ttu-id="8c6f5-282">**pbuf** è un puntatore a una stringa con terminazione null che specifica il nome del processo di stampa, ad esempio "MS-WORD: Review.doc".</span><span class="sxs-lookup"><span data-stu-id="8c6f5-282">**pBuf** is a pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>                                                                                                                        | <span data-ttu-id="8c6f5-283">0x0D</span><span class="sxs-lookup"><span data-stu-id="8c6f5-283">0x0D</span></span>  |
| <span data-ttu-id="8c6f5-284">\_ \_ priorità campo notifica \_ processi</span><span class="sxs-lookup"><span data-stu-id="8c6f5-284">JOB\_NOTIFY\_FIELD\_PRIORITY</span></span>             | <span data-ttu-id="8c6f5-285">**adwData** \[ 0 \] specifica la priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-285">**adwData** \[0\] specifies the job priority.</span></span>                                                                                                                                                                                                           | <span data-ttu-id="8c6f5-286">0x0E</span><span class="sxs-lookup"><span data-stu-id="8c6f5-286">0x0E</span></span>  |
| <span data-ttu-id="8c6f5-287">\_ \_ posizione campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-287">JOB\_NOTIFY\_FIELD\_POSITION</span></span>             | <span data-ttu-id="8c6f5-288">**adwData** \[ 0 \] specifica la posizione del processo nella coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-288">**adwData** \[0\] specifies the job's position in the print queue.</span></span>                                                                                                                                                                                      | <span data-ttu-id="8c6f5-289">0x0F</span><span class="sxs-lookup"><span data-stu-id="8c6f5-289">0x0F</span></span>  |
| <span data-ttu-id="8c6f5-290">\_campo notifica \_ processi \_ inviato</span><span class="sxs-lookup"><span data-stu-id="8c6f5-290">JOB\_NOTIFY\_FIELD\_SUBMITTED</span></span>            | <span data-ttu-id="8c6f5-291">**pbuf** è un puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora in cui è stato inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-291">**pBuf** is a pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>                                                                                                                          | <span data-ttu-id="8c6f5-292">0x10</span><span class="sxs-lookup"><span data-stu-id="8c6f5-292">0x10</span></span>  |
| <span data-ttu-id="8c6f5-293">\_ora di \_ \_ inizio campo notifica processo \_</span><span class="sxs-lookup"><span data-stu-id="8c6f5-293">JOB\_NOTIFY\_FIELD\_START\_TIME</span></span>          | <span data-ttu-id="8c6f5-294">**adwData** \[ 0 \] specifica la prima volta che il processo può essere stampato.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-294">**adwData** \[0\] specifies the earliest time that the job can be printed.</span></span> <span data-ttu-id="8c6f5-295">(Questo valore viene specificato in minuti trascorsi dalle ore 12:00)</span><span class="sxs-lookup"><span data-stu-id="8c6f5-295">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                | <span data-ttu-id="8c6f5-296">0x11</span><span class="sxs-lookup"><span data-stu-id="8c6f5-296">0x11</span></span>  |
| <span data-ttu-id="8c6f5-297">\_campo notifica \_ processo \_ fino al \_ momento</span><span class="sxs-lookup"><span data-stu-id="8c6f5-297">JOB\_NOTIFY\_FIELD\_UNTIL\_TIME</span></span>          | <span data-ttu-id="8c6f5-298">**adwData** \[ 0 \] specifica l'ora più recente in cui è possibile stampare il processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-298">**adwData** \[0\] specifies the latest time that the job can be printed.</span></span> <span data-ttu-id="8c6f5-299">(Questo valore viene specificato in minuti trascorsi dalle ore 12:00)</span><span class="sxs-lookup"><span data-stu-id="8c6f5-299">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                  | <span data-ttu-id="8c6f5-300">0x12</span><span class="sxs-lookup"><span data-stu-id="8c6f5-300">0x12</span></span>  |
| <span data-ttu-id="8c6f5-301">\_ \_ tempo campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-301">JOB\_NOTIFY\_FIELD\_TIME</span></span>                 | <span data-ttu-id="8c6f5-302">**adwData** \[ 0 \] specifica il tempo totale, in secondi, trascorso dall'inizio della stampa del processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-302">**adwData** \[0\] specifies the total time, in seconds, that has elapsed since the job began printing.</span></span>                                                                                                                                                  | <span data-ttu-id="8c6f5-303">0x13</span><span class="sxs-lookup"><span data-stu-id="8c6f5-303">0x13</span></span>  |
| <span data-ttu-id="8c6f5-304">\_ \_ \_ pagine totali campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-304">JOB\_NOTIFY\_FIELD\_TOTAL\_PAGES</span></span>         | <span data-ttu-id="8c6f5-305">**adwData** \[ 0 \] specifica le dimensioni, in pagine, del processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-305">**adwData** \[0\] specifies the size, in pages, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="8c6f5-306">0x14</span><span class="sxs-lookup"><span data-stu-id="8c6f5-306">0x14</span></span>  |
| <span data-ttu-id="8c6f5-307">pagine di campo di notifica del processo \_ \_ \_ \_ stampate</span><span class="sxs-lookup"><span data-stu-id="8c6f5-307">JOB\_NOTIFY\_FIELD\_PAGES\_PRINTED</span></span>       | <span data-ttu-id="8c6f5-308">**adwData** \[ 0 \] specifica il numero di pagine stampate.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-308">**adwData** \[0\] specifies the number of pages that have printed.</span></span>                                                                                                                                                                                      | <span data-ttu-id="8c6f5-309">0x15</span><span class="sxs-lookup"><span data-stu-id="8c6f5-309">0x15</span></span>  |
| <span data-ttu-id="8c6f5-310">\_ \_ \_ byte totali campo notifica \_ processo</span><span class="sxs-lookup"><span data-stu-id="8c6f5-310">JOB\_NOTIFY\_FIELD\_TOTAL\_BYTES</span></span>         | <span data-ttu-id="8c6f5-311">**adwData** \[ 0 \] specifica la dimensione, in byte, del processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-311">**adwData** \[0\] specifies the size, in bytes, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="8c6f5-312">0x16</span><span class="sxs-lookup"><span data-stu-id="8c6f5-312">0x16</span></span>  |
| <span data-ttu-id="8c6f5-313">\_ \_ byte campo notifica \_ processi \_ stampati</span><span class="sxs-lookup"><span data-stu-id="8c6f5-313">JOB\_NOTIFY\_FIELD\_BYTES\_PRINTED</span></span>       | <span data-ttu-id="8c6f5-314">**adwData** \[ 0 \] specifica il numero di byte che sono stati stampati in questo processo.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-314">**adwData** \[0\] specifies the number of bytes that have been printed on this job.</span></span> <span data-ttu-id="8c6f5-315">Per questo campo, l'oggetto notifica di modifica viene segnalato quando i byte vengono inviati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="8c6f5-315">For this field, the change notification object is signaled when bytes are sent to the printer.</span></span>                                                                      | <span data-ttu-id="8c6f5-316">0x17</span><span class="sxs-lookup"><span data-stu-id="8c6f5-316">0x17</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="8c6f5-317">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c6f5-317">Requirements</span></span>



| <span data-ttu-id="8c6f5-318">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c6f5-318">Requirement</span></span> | <span data-ttu-id="8c6f5-319">Valore</span><span class="sxs-lookup"><span data-stu-id="8c6f5-319">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6f5-320">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c6f5-320">Minimum supported client</span></span><br/> | <span data-ttu-id="8c6f5-321">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8c6f5-321">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8c6f5-322">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c6f5-322">Minimum supported server</span></span><br/> | <span data-ttu-id="8c6f5-323">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8c6f5-323">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8c6f5-324">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c6f5-324">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c6f5-325"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c6f5-325"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c6f5-326">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c6f5-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6f5-327">Stampa</span><span class="sxs-lookup"><span data-stu-id="8c6f5-327">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8c6f5-328">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="8c6f5-328">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="8c6f5-329">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-329">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="8c6f5-330">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-330">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="8c6f5-331">**Informazioni sul processo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-331">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="8c6f5-332">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-332">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="8c6f5-333">**\_informazioni notifica \_ stampante**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-333">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="8c6f5-334">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-334">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="8c6f5-335">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="8c6f5-335">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

