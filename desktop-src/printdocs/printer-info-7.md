---
description: La \_ struttura Printer Info \_ 7 specifica le informazioni sulla stampante dei servizi directory.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: Struttura PRINTER_INFO_7 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318027"
---
# <a name="printer_info_7-structure"></a><span data-ttu-id="e8296-103">\_Struttura info stampa \_ 7</span><span class="sxs-lookup"><span data-stu-id="e8296-103">PRINTER\_INFO\_7 structure</span></span>

<span data-ttu-id="e8296-104">La struttura **Printer \_ info \_ 7** specifica le informazioni sulla stampante dei servizi directory.</span><span class="sxs-lookup"><span data-stu-id="e8296-104">The **PRINTER\_INFO\_7** structure specifies directory services printer information.</span></span> <span data-ttu-id="e8296-105">Usare questa struttura con la funzione [**Seprinter**](setprinter.md) per pubblicare i dati di una stampante nel servizio directory (DS) o per aggiornare o rimuovere i dati pubblicati di una stampante dal DS.</span><span class="sxs-lookup"><span data-stu-id="e8296-105">Use this structure with the [**SetPrinter**](setprinter.md) function to publish a printer's data in the directory service (DS), or to update or remove a printer's published data from the DS.</span></span> <span data-ttu-id="e8296-106">Usare questa struttura con la funzione [**GetPrinter**](getprinter.md) per determinare se una stampante è pubblicata nei servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e8296-106">Use this structure with the [**GetPrinter**](getprinter.md) function to determine whether a printer is published in the DS.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8296-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8296-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a><span data-ttu-id="e8296-108">Members</span><span class="sxs-lookup"><span data-stu-id="e8296-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e8296-109">**pszObjectGUID**</span><span class="sxs-lookup"><span data-stu-id="e8296-109">**pszObjectGUID**</span></span>
</dt> <dd>

<span data-ttu-id="e8296-110">Puntatore a una stringa con terminazione null che contiene il GUID dell'oggetto coda di stampa del servizio directory associato a una stampante pubblicata.</span><span class="sxs-lookup"><span data-stu-id="e8296-110">A pointer to a null-terminated string containing the GUID of the directory service print queue object associated with a published printer.</span></span> <span data-ttu-id="e8296-111">Usare la funzione [**GetPrinter**](getprinter.md) per recuperare questo GUID.</span><span class="sxs-lookup"><span data-stu-id="e8296-111">Use the [**GetPrinter**](getprinter.md) function to retrieve this GUID.</span></span>

<span data-ttu-id="e8296-112">Prima di chiamare il [**Seprinter**](setprinter.md), impostare **pszObjectGUID** su **null**.</span><span class="sxs-lookup"><span data-stu-id="e8296-112">Before calling [**SetPrinter**](setprinter.md), set **pszObjectGUID** to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e8296-113">**dwAction**</span><span class="sxs-lookup"><span data-stu-id="e8296-113">**dwAction**</span></span>
</dt> <dd>

<span data-ttu-id="e8296-114">Indica l'azione da eseguire per la funzione [**Seprinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="e8296-114">Indicates the action for the [**SetPrinter**](setprinter.md) function to perform.</span></span> <span data-ttu-id="e8296-115">Per la funzione [**GetPrinter**](getprinter.md) , questo membro indica se la stampante specificata è pubblicata.</span><span class="sxs-lookup"><span data-stu-id="e8296-115">For the [**GetPrinter**](getprinter.md) function, this member indicates whether the specified printer is published.</span></span> <span data-ttu-id="e8296-116">Questo membro può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8296-116">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="e8296-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e8296-117">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="e8296-118">Significato</span><span class="sxs-lookup"><span data-stu-id="e8296-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <span data-ttu-id="e8296-119"><dt>**DSPRINT \_ 0x80000000 in sospeso**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e8296-119"><dt>**DSPRINT\_PENDING**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="e8296-120">[**GetPrinter**](getprinter.md): indica che il sistema sta tentando di completare un'operazione di pubblicazione o di pubblicazione non pubblicata avviata da una chiamata di [**seprinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="e8296-120">[**GetPrinter**](getprinter.md): Indicates that the system is attempting to complete a publish or unpublish operation started by a [**SetPrinter**](setprinter.md) call.</span></span><br/> <span data-ttu-id="e8296-121">[**Seprinter**](setprinter.md): questo valore non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8296-121">[**SetPrinter**](setprinter.md): This value is not valid.</span></span> <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <span data-ttu-id="e8296-122"><dt>**DSPRINT \_ PUBBLICA**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e8296-122"><dt>**DSPRINT\_PUBLISH**</dt> <dt>0x00000001</dt></span></span> </dl>       | <span data-ttu-id="e8296-123">[**Seprinter**](setprinter.md): pubblica i dati della stampante in DS.</span><span class="sxs-lookup"><span data-stu-id="e8296-123">[**SetPrinter**](setprinter.md): Publishes the printer's data in the DS.</span></span><br/> <span data-ttu-id="e8296-124">[**GetPrinter**](getprinter.md): indica che la stampante è pubblicata.</span><span class="sxs-lookup"><span data-stu-id="e8296-124">[**GetPrinter**](getprinter.md): Indicates the printer is published.</span></span> <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <span data-ttu-id="e8296-125"><dt>**DSPRINT \_ Ripubblicare**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="e8296-125"><dt>**DSPRINT\_REPUBLISH**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="e8296-126">[**Seprinter**](setprinter.md): i dati DS per la stampante non sono pubblicati e quindi pubblicati nuovamente, aggiornando tutte le proprietà nella stampante pubblicata.</span><span class="sxs-lookup"><span data-stu-id="e8296-126">[**SetPrinter**](setprinter.md): The DS data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="e8296-127">La ripubblicazione modifica anche il GUID della stampante pubblicata.</span><span class="sxs-lookup"><span data-stu-id="e8296-127">Re-publishing also changes the GUID of the published printer.</span></span><br/> <span data-ttu-id="e8296-128">[**GetPrinter**](getprinter.md): non restituisce mai questo valore.</span><span class="sxs-lookup"><span data-stu-id="e8296-128">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <span data-ttu-id="e8296-129"><dt>**DSPRINT \_ Annulla pubblicazione**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="e8296-129"><dt>**DSPRINT\_UNPUBLISH**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="e8296-130">[**Seprinter**](setprinter.md): rimuove i dati pubblicati dalla stampante dal DS.</span><span class="sxs-lookup"><span data-stu-id="e8296-130">[**SetPrinter**](setprinter.md): Removes the printer's published data from the DS.</span></span><br/> <span data-ttu-id="e8296-131">[**GetPrinter**](getprinter.md): indica che la stampante non è pubblicata.</span><span class="sxs-lookup"><span data-stu-id="e8296-131">[**GetPrinter**](getprinter.md): Indicates the printer is not published.</span></span> <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <span data-ttu-id="e8296-132"><dt>**DSPRINT \_ AGGIORNARE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e8296-132"><dt>**DSPRINT\_UPDATE**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="e8296-133">[**Seprinter**](setprinter.md): Aggiorna i dati pubblicati della stampante in DS.</span><span class="sxs-lookup"><span data-stu-id="e8296-133">[**SetPrinter**](setprinter.md): Updates the printer's published data in the DS.</span></span><br/> <span data-ttu-id="e8296-134">[**GetPrinter**](getprinter.md): non restituisce mai questo valore.</span><span class="sxs-lookup"><span data-stu-id="e8296-134">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8296-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8296-135">Remarks</span></span>

<span data-ttu-id="e8296-136">La struttura delle **informazioni di stampa \_ \_ 7** viene utilizzata in una chiamata del [**seprinter**](setprinter.md) per pubblicare le informazioni sulla stampante nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="e8296-136">The **PRINTER\_INFO\_7** structure is used in a [**SetPrinter**](setprinter.md) call to publish printer information to the directory service.</span></span> <span data-ttu-id="e8296-137">I dati pubblicati includono tutti i valori e i dati per la stampante specificata, disponibile nella \_ chiave dello spooler SPLDS, nella chiave del \_ \_ driver SPLDS o nelle \_ \_ \_ chiavi chiave utente SPLDS create da [**SetPrinterDataEx**](setprinterdataex.md).</span><span class="sxs-lookup"><span data-stu-id="e8296-137">The published data includes all values and data for the specified printer found under the SPLDS\_SPOOLER\_KEY, SPLDS\_DRIVER\_KEY, or SPLDS\_USER\_KEY keys created by [**SetPrinterDataEx**](setprinterdataex.md).</span></span>

<span data-ttu-id="e8296-138">Per [**Seprinter**](setprinter.md), *pszObjectGUID* deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="e8296-138">For [**SetPrinter**](setprinter.md), *pszObjectGUID* should be set to **NULL**.</span></span> <span data-ttu-id="e8296-139">Per [**GetPrinter**](getprinter.md), *PSZOBJECTGUID* restituisce il GUID dell'oggetto coda di stampa dei servizi directory associato a una stampante pubblicata.</span><span class="sxs-lookup"><span data-stu-id="e8296-139">For [**GetPrinter**](getprinter.md), *pszObjectGUID* returns the GUID of the directory services print queue object associated with a published printer.</span></span> <span data-ttu-id="e8296-140">È possibile utilizzare questo GUID con i metodi Active Directory Services Interface (ADSI) per recuperare i dati pubblicati per la stampante.</span><span class="sxs-lookup"><span data-stu-id="e8296-140">You can use this GUID with Active Directory Services Interface (ADSI) methods to retrieve published data for the printer.</span></span> <span data-ttu-id="e8296-141">Tuttavia, il metodo consigliato per il recupero dei dati pubblicati consiste nel chiamare la funzione [**GetPrinterDataEx**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="e8296-141">However, the recommended method for retrieving published data is to call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8296-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8296-142">Requirements</span></span>



| <span data-ttu-id="e8296-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8296-143">Requirement</span></span> | <span data-ttu-id="e8296-144">Valore</span><span class="sxs-lookup"><span data-stu-id="e8296-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8296-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8296-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e8296-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8296-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e8296-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8296-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e8296-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8296-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e8296-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8296-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8296-150"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8296-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e8296-151">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e8296-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e8296-152">**\_ Informazioni sulle stampanti \_ \_ 7W** (Unicode) e **\_ \_ Info stampante \_ 7a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e8296-152">**\_PRINTER\_INFO\_7W** (Unicode) and **\_PRINTER\_INFO\_7A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="e8296-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8296-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8296-154">Stampa</span><span class="sxs-lookup"><span data-stu-id="e8296-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e8296-155">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="e8296-155">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




