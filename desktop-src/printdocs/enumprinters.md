---
description: La funzione EnumPrinters enumera le stampanti disponibili, i server di stampa, i domini o i provider di stampa.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Funzione EnumPrinters (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881614"
---
# <a name="enumprinters-function"></a><span data-ttu-id="11443-103">EnumPrinters (funzione)</span><span class="sxs-lookup"><span data-stu-id="11443-103">EnumPrinters function</span></span>

<span data-ttu-id="11443-104">La funzione **EnumPrinters** enumera le stampanti disponibili, i server di stampa, i domini o i provider di stampa.</span><span class="sxs-lookup"><span data-stu-id="11443-104">The **EnumPrinters** function enumerates available printers, print servers, domains, or print providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="11443-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11443-105">Syntax</span></span>


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="11443-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="11443-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11443-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11443-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11443-108">Tipi di oggetti di stampa che la funzione deve enumerare.</span><span class="sxs-lookup"><span data-stu-id="11443-108">The types of print objects that the function should enumerate.</span></span> <span data-ttu-id="11443-109">Questo valore può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="11443-109">This value can be one or more of the following values.</span></span>



| <span data-ttu-id="11443-110">Valore</span><span class="sxs-lookup"><span data-stu-id="11443-110">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="11443-111">Significato</span><span class="sxs-lookup"><span data-stu-id="11443-111">Meaning</span></span>                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <span data-ttu-id="11443-112"><dt>**\_enumerazione stampante \_ locale**</dt></span><span class="sxs-lookup"><span data-stu-id="11443-112"><dt>**PRINTER\_ENUM\_LOCAL**</dt></span></span> </dl>                       | <span data-ttu-id="11443-113">Se \_ \_ non viene passato anche il flag del nome enum della stampante, la funzione ignora il parametro *Name* ed enumera le stampanti installate localmente.</span><span class="sxs-lookup"><span data-stu-id="11443-113">If the PRINTER\_ENUM\_NAME flag is not also passed, the function ignores the *Name* parameter, and enumerates the locally installed printers.</span></span> <span data-ttu-id="11443-114">Se \_ viene passato anche il nome dell'enum della stampante \_ , la funzione enumera le stampanti locali nel *nome*.</span><span class="sxs-lookup"><span data-stu-id="11443-114">If PRINTER\_ENUM\_NAME is also passed, the function enumerates the local printers on *Name*.</span></span> <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <span data-ttu-id="11443-115"><dt>**\_Nome enum \_ stampante**</dt></span><span class="sxs-lookup"><span data-stu-id="11443-115"><dt>**PRINTER\_ENUM\_NAME**</dt></span></span> </dl>                          | <span data-ttu-id="11443-116">La funzione enumera la stampante identificata in base al *nome*.</span><span class="sxs-lookup"><span data-stu-id="11443-116">The function enumerates the printer identified by *Name*.</span></span> <span data-ttu-id="11443-117">Può trattarsi di un server, di un dominio o di un provider di stampa.</span><span class="sxs-lookup"><span data-stu-id="11443-117">This can be a server, a domain, or a print provider.</span></span> <span data-ttu-id="11443-118">Se *Name* è **null**, la funzione enumera i provider di stampa disponibili.</span><span class="sxs-lookup"><span data-stu-id="11443-118">If *Name* is **NULL**, the function enumerates available print providers.</span></span><br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <span data-ttu-id="11443-119"><dt>**\_enumerazione stampante \_ condivisa**</dt></span><span class="sxs-lookup"><span data-stu-id="11443-119"><dt>**PRINTER\_ENUM\_SHARED**</dt></span></span> </dl>                    | <span data-ttu-id="11443-120">La funzione enumera le stampanti che dispongono dell'attributo Shared.</span><span class="sxs-lookup"><span data-stu-id="11443-120">The function enumerates printers that have the shared attribute.</span></span> <span data-ttu-id="11443-121">Non può essere usato in isolamento; utilizzare un'operazione o per combinare con un altro \_ tipo di enumerazione Printer.</span><span class="sxs-lookup"><span data-stu-id="11443-121">Cannot be used in isolation; use an OR operation to combine with another PRINTER\_ENUM type.</span></span><br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <span data-ttu-id="11443-122"><dt>**\_connessioni enum \_ stampanti**</dt></span><span class="sxs-lookup"><span data-stu-id="11443-122"><dt>**PRINTER\_ENUM\_CONNECTIONS**</dt></span></span> </dl>     | <span data-ttu-id="11443-123">La funzione enumera l'elenco di stampanti a cui l'utente ha eseguito le connessioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="11443-123">The function enumerates the list of printers to which the user has made previous connections.</span></span><br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <span data-ttu-id="11443-124"><dt>**\_rete enum \_ Printer**</dt></span><span class="sxs-lookup"><span data-stu-id="11443-124"><dt>**PRINTER\_ENUM\_NETWORK**</dt></span></span> </dl>                 | <span data-ttu-id="11443-125">La funzione enumera le stampanti di rete nel dominio del computer.</span><span class="sxs-lookup"><span data-stu-id="11443-125">The function enumerates network printers in the computer's domain.</span></span> <span data-ttu-id="11443-126">Questo valore è valido solo se *Level* è 1.</span><span class="sxs-lookup"><span data-stu-id="11443-126">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <span data-ttu-id="11443-127"><dt>**\_enumerazione stampanti \_ Remote**</dt></span><span class="sxs-lookup"><span data-stu-id="11443-127"><dt>**PRINTER\_ENUM\_REMOTE**</dt></span></span> </dl>                    | <span data-ttu-id="11443-128">La funzione enumera le stampanti di rete e i server di stampa nel dominio del computer.</span><span class="sxs-lookup"><span data-stu-id="11443-128">The function enumerates network printers and print servers in the computer's domain.</span></span> <span data-ttu-id="11443-129">Questo valore è valido solo se *Level* è 1.</span><span class="sxs-lookup"><span data-stu-id="11443-129">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <span data-ttu-id="11443-130"><dt>**\_Categoria enumerazione \_ stampanti \_ 3D**</dt></span><span class="sxs-lookup"><span data-stu-id="11443-130"><dt>**PRINTER\_ENUM\_CATEGORY\_3D**</dt></span></span> </dl>    | <span data-ttu-id="11443-131">La funzione enumera solo le stampanti 3D.</span><span class="sxs-lookup"><span data-stu-id="11443-131">The function enumerates only 3D printers.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <span data-ttu-id="11443-132"><dt>**\_categoria enum \_ stampanti \_ All**</dt></span><span class="sxs-lookup"><span data-stu-id="11443-132"><dt>**PRINTER\_ENUM\_CATEGORY\_ALL**</dt></span></span> </dl> | <span data-ttu-id="11443-133">La funzione enumera tutti i dispositivi di stampa, incluse le stampanti 3D.</span><span class="sxs-lookup"><span data-stu-id="11443-133">The function enumerates all print devices, including 3D printers.</span></span><br/>                                                                                                                                                                           |



 

<span data-ttu-id="11443-134">Se *Level* è 4, è possibile utilizzare solo le \_ \_ costanti locali Printer enum Connections e Printer \_ enum \_ .</span><span class="sxs-lookup"><span data-stu-id="11443-134">If *Level* is 4, you can only use the PRINTER\_ENUM\_CONNECTIONS and PRINTER\_ENUM\_LOCAL constants.</span></span>

> [!Note]  
> <span data-ttu-id="11443-135">i dispositivi di stampa 3D non vengono enumerati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="11443-135">3D print devices are not enumerated by default.</span></span> <span data-ttu-id="11443-136">Per enumerare solo le stampanti 3D, è necessario includere sia la **\_ categoria di enumerazione stampanti \_ \_ 3D** che la **stampante \_ enum \_ local** .</span><span class="sxs-lookup"><span data-stu-id="11443-136">You must include both **PRINTER\_ENUM\_CATEGORY\_3D** and **PRINTER\_ENUM\_LOCAL** to enumerate only 3D printers.</span></span> <span data-ttu-id="11443-137">Per includere stampanti 3D, insieme a tutte le altre stampanti locali, utilizzare **Printer \_ enum \_ Category \_ All** e **Printer \_ enum \_ local**.</span><span class="sxs-lookup"><span data-stu-id="11443-137">To include 3D printers, along with all other local printers, use **PRINTER\_ENUM\_CATEGORY\_ALL** and **PRINTER\_ENUM\_LOCAL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="11443-138">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11443-138">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11443-139">Se *Level* è 1, *Flags* contiene \_ il nome enum della stampante \_ e il *nome* è diverso da **null**, il *nome* è un puntatore a una stringa con terminazione null che specifica il nome dell'oggetto da enumerare.</span><span class="sxs-lookup"><span data-stu-id="11443-139">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is non-**NULL**, then *Name* is a pointer to a null-terminated string that specifies the name of the object to enumerate.</span></span> <span data-ttu-id="11443-140">Questa stringa può essere il nome di un server, di un dominio o di un provider di stampa.</span><span class="sxs-lookup"><span data-stu-id="11443-140">This string can be the name of a server, a domain, or a print provider.</span></span>

<span data-ttu-id="11443-141">Se *Level* è 1, *Flags* contiene \_ il nome enum della stampante \_ e *Name* è **null**, la funzione enumera i provider di stampa disponibili.</span><span class="sxs-lookup"><span data-stu-id="11443-141">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is **NULL**, then the function enumerates the available print providers.</span></span>

<span data-ttu-id="11443-142">Se *Level* è 1, *Flags* contiene Printer \_ enum \_ remote e *Name* è **null**, la funzione enumera le stampanti nel dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="11443-142">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_REMOTE, and *Name* is **NULL**, then the function enumerates the printers in the user's domain.</span></span>

<span data-ttu-id="11443-143">Se *Level* è 2 o 5,*Name* è un puntatore a una stringa con terminazione null che specifica il nome di un server di cui è necessario enumerare le stampanti.</span><span class="sxs-lookup"><span data-stu-id="11443-143">If *Level* is 2 or 5,*Name* is a pointer to a null-terminated string that specifies the name of a server whose printers are to be enumerated.</span></span> <span data-ttu-id="11443-144">Se questa stringa è **null**, la funzione enumera le stampanti installate nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="11443-144">If this string is **NULL**, then the function enumerates the printers installed on the local computer.</span></span>

<span data-ttu-id="11443-145">Se *Level* è 4, il *nome* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="11443-145">If *Level* is 4, *Name* should be **NULL**.</span></span> <span data-ttu-id="11443-146">La funzione esegue sempre query sul computer locale.</span><span class="sxs-lookup"><span data-stu-id="11443-146">The function always queries on the local computer.</span></span>

<span data-ttu-id="11443-147">Quando *Name* è **null**, l'impostazione dei *flag* per Printer \_ enum \_ Local \| Printer \_ enum \_ Connections enumera le stampanti installate nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="11443-147">When *Name* is **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_CONNECTIONS enumerates printers that are installed on the local machine.</span></span> <span data-ttu-id="11443-148">Queste stampanti includono quelle fisicamente collegate al computer locale e le stampanti remote a cui ha una connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="11443-148">These printers include those that are physically attached to the local machine as well as remote printers to which it has a network connection.</span></span>

<span data-ttu-id="11443-149">Quando il *nome* non è **null**, l'impostazione dei *flag* sul \_ \_ Nome enum della stampante locale enum \| \_ \_ enumera le stampanti locali installate nel *nome* del server.</span><span class="sxs-lookup"><span data-stu-id="11443-149">When *Name* is not **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_NAME enumerates the local printers that are installed on the server *Name*.</span></span>

</dd> <dt>

<span data-ttu-id="11443-150">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="11443-150">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11443-151">Tipo di strutture di dati a cui punta *pPrinterEnum*.</span><span class="sxs-lookup"><span data-stu-id="11443-151">The type of data structures pointed to by *pPrinterEnum*.</span></span> <span data-ttu-id="11443-152">I valori validi sono 1, 2, 4 e 5, che corrispondono alle strutture di dati Printer Info [**\_ \_ 1**](printer-info-1.md), [**Printer \_ info \_ 2**](printer-info-2.md) , [**Printer \_ info \_ 4**](printer-info-4.md)e [**Printer \_ info \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="11443-152">Valid values are 1, 2, 4, and 5, which correspond to the [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), and [**PRINTER\_INFO\_5**](printer-info-5.md) data structures.</span></span>

<span data-ttu-id="11443-153">Questo valore può essere 1, 2, 4 o 5.</span><span class="sxs-lookup"><span data-stu-id="11443-153">This value can be 1, 2, 4, or 5.</span></span>

</dd> <dt>

<span data-ttu-id="11443-154">*pPrinterEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="11443-154">*pPrinterEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11443-155">Puntatore a un buffer che riceve una matrice di strutture di informazioni stampante [**\_ \_ 1**](printer-info-1.md), [**\_ informazioni stampante \_ 2**](printer-info-2.md), [**\_ informazioni stampante \_ 4**](printer-info-4.md)o [**stampanti \_ \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="11443-155">A pointer to a buffer that receives an array of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span> <span data-ttu-id="11443-156">Ogni struttura contiene dati che descrivono un oggetto Print disponibile.</span><span class="sxs-lookup"><span data-stu-id="11443-156">Each structure contains data that describes an available print object.</span></span>

<span data-ttu-id="11443-157">Se *Level* è 1, la matrice contiene le strutture delle [**informazioni di stampa \_ \_ 1**](printer-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="11443-157">If *Level* is 1, the array contains [**PRINTER\_INFO\_1**](printer-info-1.md) structures.</span></span> <span data-ttu-id="11443-158">Se *Level* è 2, la matrice contiene le strutture [**\_ info \_ 2 della stampante**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="11443-158">If *Level* is 2, the array contains [**PRINTER\_INFO\_2**](printer-info-2.md) structures.</span></span> <span data-ttu-id="11443-159">Se *Level* è 4, la matrice contiene le strutture delle [**informazioni di stampa \_ \_ 4**](printer-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="11443-159">If *Level* is 4, the array contains [**PRINTER\_INFO\_4**](printer-info-4.md) structures.</span></span> <span data-ttu-id="11443-160">Se *Level* è 5, la matrice contiene le strutture [**info della stampante \_ \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="11443-160">If *Level* is 5, the array contains [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span>

<span data-ttu-id="11443-161">Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture di dati e qualsiasi stringa o altri dati a cui puntano i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="11443-161">The buffer must be large enough to receive the array of data structures and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="11443-162">Se il buffer è troppo piccolo, il parametro *pcbNeeded* restituisce le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="11443-162">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="11443-163">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11443-163">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11443-164">Dimensione, in byte, del buffer a cui punta *pPrinterEnum*.</span><span class="sxs-lookup"><span data-stu-id="11443-164">The size, in bytes, of the buffer pointed to by *pPrinterEnum*.</span></span>

</dd> <dt>

<span data-ttu-id="11443-165">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="11443-165">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11443-166">Puntatore a un valore che riceve il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="11443-166">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="11443-167">*pcReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="11443-167">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11443-168">Puntatore a un valore che riceve il numero di strutture per le informazioni sulle stampanti [**\_ \_ 1**](printer-info-1.md), le informazioni sulla stampante [**\_ \_ 2**](printer-info-2.md) , le informazioni sulla stampante [**\_ \_ 4**](printer-info-4.md)o le [**informazioni della stampante \_ \_ 5**](printer-info-5.md) che la funzione restituisce nella matrice a cui punta *pPrinterEnum* .</span><span class="sxs-lookup"><span data-stu-id="11443-168">A pointer to a value that receives the number of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures that the function returns in the array to which *pPrinterEnum* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11443-169">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11443-169">Return value</span></span>

<span data-ttu-id="11443-170">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="11443-170">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="11443-171">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="11443-171">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="11443-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="11443-172">Remarks</span></span>

<span data-ttu-id="11443-173">Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="11443-173">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="11443-174">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="11443-174">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="11443-175">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="11443-175">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="11443-176">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="11443-176">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="11443-177">Se **EnumPrinters** restituisce una struttura [**Printer \_ info \_ 1**](printer-info-1.md) in cui \_ è specificato il contenitore enum della stampante \_ , significa che esiste una gerarchia di oggetti Printer.</span><span class="sxs-lookup"><span data-stu-id="11443-177">If **EnumPrinters** returns a [**PRINTER\_INFO\_1**](printer-info-1.md) structure in which PRINTER\_ENUM\_CONTAINER is specified, this indicates that there is a hierarchy of printer objects.</span></span> <span data-ttu-id="11443-178">Un'applicazione può enumerare la gerarchia chiamando di nuovo **EnumPrinters** , impostando *Name* sul valore del membro **pname** della struttura **Printer \_ info \_ 1** .</span><span class="sxs-lookup"><span data-stu-id="11443-178">An application can enumerate the hierarchy by calling **EnumPrinters** again, setting *Name* to the value of the **PRINTER\_INFO\_1** structure's **pName** member.</span></span>

<span data-ttu-id="11443-179">La funzione **EnumPrinters** non recupera le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="11443-179">The **EnumPrinters** function does not retrieve security information.</span></span> <span data-ttu-id="11443-180">Se le strutture [**\_ info \_ 2 della stampante**](printer-info-2.md) vengono restituite nella matrice a cui punta *PPrinterEnum*, i relativi membri *pSecurityDescriptor* verranno impostati su **null**.</span><span class="sxs-lookup"><span data-stu-id="11443-180">If [**PRINTER\_INFO\_2**](printer-info-2.md) structures are returned in the array pointed to by *pPrinterEnum*, their *pSecurityDescriptor* members will be set to **NULL**.</span></span>

<span data-ttu-id="11443-181">Per ottenere informazioni sulla stampante predefinita, chiamare [**GetDefaultPrinter**](getdefaultprinter.md).</span><span class="sxs-lookup"><span data-stu-id="11443-181">To get information about the default printer, call [**GetDefaultPrinter**](getdefaultprinter.md).</span></span>

<span data-ttu-id="11443-182">La struttura delle [**informazioni di stampa \_ \_ 4**](printer-info-4.md) fornisce un metodo semplice ed estremamente rapido per recuperare i nomi delle stampanti installate in un computer locale, nonché le connessioni remote stabilite da un utente.</span><span class="sxs-lookup"><span data-stu-id="11443-182">The [**PRINTER\_INFO\_4**](printer-info-4.md) structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="11443-183">Quando **EnumPrinters** viene chiamato con una struttura di dati **Printer \_ info \_ 4** , tale funzione esegue una query sul Registro di sistema per ottenere le informazioni specificate, quindi restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="11443-183">When **EnumPrinters** is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="11443-184">Questo comportamento è diverso da quello di **EnumPrinters** quando viene chiamato con altri livelli di **informazioni sulle stampanti \_ \_ \* *_ strutture dei dati. In particolare, quando _* EnumPrinters** viene chiamato con una struttura di dati di livello 2 ([**Printer \_ info \_ 2**](printer-info-2.md)), esegue una chiamata [**OpenPrinter**](openprinter.md) su ogni connessione remota.</span><span class="sxs-lookup"><span data-stu-id="11443-184">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_\**_ data structures. In particular, when _\* EnumPrinters*\* is called with a level 2 ([**PRINTER\_INFO\_2**](printer-info-2.md)) data structure, it performs an [**OpenPrinter**](openprinter.md) call on each remote connection.</span></span> <span data-ttu-id="11443-185">Se una connessione remota non è attiva o il server remoto non esiste più oppure la stampante remota non esiste più, la funzione deve attendere il timeout di RPC e, di conseguenza, interrompere la chiamata **OpenPrinter** .</span><span class="sxs-lookup"><span data-stu-id="11443-185">If a remote connection is down, or the remote server no longer exists, or the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="11443-186">L'operazione può richiedere un po' di tempo.</span><span class="sxs-lookup"><span data-stu-id="11443-186">This can take a while.</span></span> <span data-ttu-id="11443-187">Il passaggio di una struttura **Printer \_ info \_ 4** consente a un'applicazione di recuperare un minimo di informazioni obbligatorie; se si desidera ottenere informazioni più dettagliate, è possibile effettuare una chiamata di **EnumPrinters** Level 2 successiva.</span><span class="sxs-lookup"><span data-stu-id="11443-187">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinters** level 2 call can be made.</span></span>

<span data-ttu-id="11443-188">**Windows Vista:** I dati della stampante restituiti da **EnumPrinters** vengono recuperati da una cache locale quando il valore di *Level* è 4.</span><span class="sxs-lookup"><span data-stu-id="11443-188">**Windows Vista:** The printer data returned by **EnumPrinters** is retrieved from a local cache when the value of *Level* is 4.</span></span>

<span data-ttu-id="11443-189">La tabella seguente mostra l'output di **EnumPrinters** per i diversi valori di *flag* quando il parametro *Level* è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="11443-189">The following table shows the **EnumPrinters** output for various *Flags* values when the *Level* parameter is set to 1.</span></span>

<span data-ttu-id="11443-190">Nella colonna parametro *nome* della tabella è necessario sostituire un nome appropriato per provider di stampa, dominio e computer.</span><span class="sxs-lookup"><span data-stu-id="11443-190">In the *Name* parameter column of the table, you should substitute an appropriate name for Print Provider, Domain, and Machine.</span></span> <span data-ttu-id="11443-191">Per "Print Provider", ad esempio, è possibile utilizzare il nome del provider di stampa di rete o il nome del provider di stampa locale.</span><span class="sxs-lookup"><span data-stu-id="11443-191">For example, for "Print Provider," you could use the name of the network print provider or the name of the local print provider.</span></span> <span data-ttu-id="11443-192">Per recuperare i nomi dei provider di stampa, chiamare **EnumPrinters** con il *nome* impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="11443-192">To retrieve print provider names, call **EnumPrinters** with *Name* set to **NULL**.</span></span>



| <span data-ttu-id="11443-193">*Flags* -parametro</span><span class="sxs-lookup"><span data-stu-id="11443-193">*Flags* parameter</span></span>                                  | <span data-ttu-id="11443-194">Parametro del *nome*</span><span class="sxs-lookup"><span data-stu-id="11443-194">*Name* parameter</span></span>                            | <span data-ttu-id="11443-195">Risultato</span><span class="sxs-lookup"><span data-stu-id="11443-195">Result</span></span>                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11443-196">PRINTER \_ enum \_ locale (e non \_ Nome enum Printer \_ )</span><span class="sxs-lookup"><span data-stu-id="11443-196">PRINTER\_ENUM\_LOCAL (and not PRINTER\_ENUM\_NAME)</span></span> | <span data-ttu-id="11443-197">Il parametro *Name* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="11443-197">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="11443-198">Tutte le stampanti locali.</span><span class="sxs-lookup"><span data-stu-id="11443-198">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="11443-199">\_Nome enum \_ stampante</span><span class="sxs-lookup"><span data-stu-id="11443-199">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="11443-200">"Provider di stampa"</span><span class="sxs-lookup"><span data-stu-id="11443-200">"Print Provider"</span></span><br/>                 | <span data-ttu-id="11443-201">Tutti i nomi di dominio</span><span class="sxs-lookup"><span data-stu-id="11443-201">All domain names</span></span><br/>                                                                       |
| <span data-ttu-id="11443-202">\_Nome enum \_ stampante</span><span class="sxs-lookup"><span data-stu-id="11443-202">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="11443-203">"Provider di stampa! Dominio</span><span class="sxs-lookup"><span data-stu-id="11443-203">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="11443-204">Tutte le stampanti e i server di stampa nel dominio del computer</span><span class="sxs-lookup"><span data-stu-id="11443-204">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="11443-205">\_Nome enum \_ stampante</span><span class="sxs-lookup"><span data-stu-id="11443-205">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="11443-206">"Provider di stampa!! \\ \\ Macchina</span><span class="sxs-lookup"><span data-stu-id="11443-206">"Print Provider!!\\\\Machine"</span></span><br/>    | <span data-ttu-id="11443-207">Tutte le stampanti condivise nel \\ \\ computer</span><span class="sxs-lookup"><span data-stu-id="11443-207">All printers shared at \\\\Machine</span></span><br/>                                                     |
| <span data-ttu-id="11443-208">\_Nome enum \_ stampante</span><span class="sxs-lookup"><span data-stu-id="11443-208">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="11443-209">Una stringa vuota ""</span><span class="sxs-lookup"><span data-stu-id="11443-209">An empty string, ""</span></span><br/>              | <span data-ttu-id="11443-210">Tutte le stampanti locali.</span><span class="sxs-lookup"><span data-stu-id="11443-210">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="11443-211">\_Nome enum \_ stampante</span><span class="sxs-lookup"><span data-stu-id="11443-211">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="11443-212">**NULL**</span><span class="sxs-lookup"><span data-stu-id="11443-212">**NULL**</span></span><br/>                         | <span data-ttu-id="11443-213">Tutti i provider di stampa nel dominio del computer</span><span class="sxs-lookup"><span data-stu-id="11443-213">All print providers in the computer's domain</span></span><br/>                                           |
| <span data-ttu-id="11443-214">\_connessioni enum \_ stampanti</span><span class="sxs-lookup"><span data-stu-id="11443-214">PRINTER\_ENUM\_CONNECTIONS</span></span>                         | <span data-ttu-id="11443-215">Il parametro *Name* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="11443-215">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="11443-216">Tutte le stampanti remote connesse</span><span class="sxs-lookup"><span data-stu-id="11443-216">All connected remote printers</span></span><br/>                                                          |
| <span data-ttu-id="11443-217">\_rete enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="11443-217">PRINTER\_ENUM\_NETWORK</span></span>                             | <span data-ttu-id="11443-218">Il parametro *Name* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="11443-218">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="11443-219">Tutte le stampanti nel dominio del computer</span><span class="sxs-lookup"><span data-stu-id="11443-219">All printers in the computer's domain</span></span><br/>                                                  |
| <span data-ttu-id="11443-220">\_enumerazione stampanti \_ Remote</span><span class="sxs-lookup"><span data-stu-id="11443-220">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="11443-221">Una stringa vuota ""</span><span class="sxs-lookup"><span data-stu-id="11443-221">An empty string, ""</span></span><br/>              | <span data-ttu-id="11443-222">Tutte le stampanti e i server di stampa nel dominio del computer</span><span class="sxs-lookup"><span data-stu-id="11443-222">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="11443-223">\_enumerazione stampanti \_ Remote</span><span class="sxs-lookup"><span data-stu-id="11443-223">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="11443-224">"Provider di stampa"</span><span class="sxs-lookup"><span data-stu-id="11443-224">"Print Provider"</span></span><br/>                 | <span data-ttu-id="11443-225">Uguale al \_ Nome enum della stampante \_</span><span class="sxs-lookup"><span data-stu-id="11443-225">Same as PRINTER\_ENUM\_NAME</span></span><br/>                                                            |
| <span data-ttu-id="11443-226">\_enumerazione stampanti \_ Remote</span><span class="sxs-lookup"><span data-stu-id="11443-226">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="11443-227">"Provider di stampa! Dominio</span><span class="sxs-lookup"><span data-stu-id="11443-227">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="11443-228">Tutte le stampanti e i server di stampa nel dominio del computer, indipendentemente dal *dominio* specificato.</span><span class="sxs-lookup"><span data-stu-id="11443-228">All printers and print servers in computer's domain, regardless of *Domain* specified.</span></span><br/> |
| <span data-ttu-id="11443-229">\_Categoria enumerazione \_ stampanti \_ 3D</span><span class="sxs-lookup"><span data-stu-id="11443-229">PRINTER\_ENUM\_CATEGORY\_3D</span></span>                        | <span data-ttu-id="11443-230">Il parametro *Name* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="11443-230">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="11443-231">Vengono enumerate solo le stampanti 3D.</span><span class="sxs-lookup"><span data-stu-id="11443-231">Only 3D printers are enumerated.</span></span><br/>                                                       |
| <span data-ttu-id="11443-232">\_categoria enum \_ stampanti \_ All</span><span class="sxs-lookup"><span data-stu-id="11443-232">PRINTER\_ENUM\_CATEGORY\_ALL</span></span>                       | <span data-ttu-id="11443-233">Il parametro *Name* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="11443-233">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="11443-234">le stampanti 3D vengono enumerate insieme a tutte le altre stampanti.</span><span class="sxs-lookup"><span data-stu-id="11443-234">3D printers are enumerated, along with all other printers.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="11443-235">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11443-235">Requirements</span></span>



| <span data-ttu-id="11443-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="11443-236">Requirement</span></span> | <span data-ttu-id="11443-237">Valore</span><span class="sxs-lookup"><span data-stu-id="11443-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11443-238">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11443-238">Minimum supported client</span></span><br/> | <span data-ttu-id="11443-239">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11443-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="11443-240">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11443-240">Minimum supported server</span></span><br/> | <span data-ttu-id="11443-241">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11443-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="11443-242">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11443-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="11443-243"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11443-243"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="11443-244">Libreria</span><span class="sxs-lookup"><span data-stu-id="11443-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="11443-245"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11443-245"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="11443-246">DLL</span><span class="sxs-lookup"><span data-stu-id="11443-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11443-247"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="11443-247"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="11443-248">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="11443-248">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="11443-249">**EnumPrintersW** (Unicode) e **EnumPrintersA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="11443-249">**EnumPrintersW** (Unicode) and **EnumPrintersA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="11443-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11443-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11443-251">Stampa</span><span class="sxs-lookup"><span data-stu-id="11443-251">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="11443-252">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="11443-252">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="11443-253">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="11443-253">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="11443-254">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="11443-254">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="11443-255">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="11443-255">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="11443-256">**\_Informazioni stampante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="11443-256">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="11443-257">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="11443-257">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="11443-258">**\_Informazioni stampante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="11443-258">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="11443-259">**\_Informazioni stampante \_ 5**</span><span class="sxs-lookup"><span data-stu-id="11443-259">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="11443-260">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="11443-260">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

