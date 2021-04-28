---
description: 'Struttura DEVICEDIALOGDATA2: definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.'
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Struttura DEVICEDIALOGDATA2 (Wiadefd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 82ca6cba81101e577eed882ad45272ab81546fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089806"
---
# <a name="devicedialogdata2-structure"></a><span data-ttu-id="e9ee8-103">Struttura DEVICEDIALOGDATA2</span><span class="sxs-lookup"><span data-stu-id="e9ee8-103">DEVICEDIALOGDATA2 structure</span></span>

<span data-ttu-id="e9ee8-104">Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ee8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9ee8-105">Syntax</span></span>


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a><span data-ttu-id="e9ee8-106">Members</span><span class="sxs-lookup"><span data-stu-id="e9ee8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9ee8-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9ee8-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ee8-109">Specifica le dimensioni della struttura in byte.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee8-110">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-110">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="e9ee8-111">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e9ee8-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="e9ee8-112">Punta a [**un'interfaccia IWiaItem2**](-wia-iwiaitem2.md) che rappresenta l'elemento radice valido nell'albero degli elementi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-112">Points to an [**IWiaItem2**](-wia-iwiaitem2.md) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee8-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e9ee8-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ee8-115">Specifica un set di flag che controllano l'operazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-115">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="e9ee8-116">Può essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9ee8-116">Can be set to any of the following values:</span></span>



| <span data-ttu-id="e9ee8-117">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="e9ee8-117">Flag</span></span>                                 | <span data-ttu-id="e9ee8-118">Significato</span><span class="sxs-lookup"><span data-stu-id="e9ee8-118">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ee8-119">0</span><span class="sxs-lookup"><span data-stu-id="e9ee8-119">0</span></span>                                    | <span data-ttu-id="e9ee8-120">Comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-120">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="e9ee8-121">IMMAGINE SINGOLA \_ DELLA FINESTRA DI DIALOGO DEL \_ \_ DISPOSITIVO \_ WIA</span><span class="sxs-lookup"><span data-stu-id="e9ee8-121">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="e9ee8-122">Limitare la selezione dell'immagine a una singola immagine nella finestra di dialogo di acquisizione dell'immagine del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-122">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="e9ee8-123">FINESTRA DI DIALOGO DEL DISPOSITIVO WIA \_ \_ - USARE \_ \_ L'INTERFACCIA \_ UTENTE COMUNE</span><span class="sxs-lookup"><span data-stu-id="e9ee8-123">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="e9ee8-124">Usare l'interfaccia utente di sistema, se disponibile, anziché l'interfaccia utente fornita dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-124">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="e9ee8-125">Se l'interfaccia utente del sistema non è disponibile, viene usata l'interfaccia utente del fornitore.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-125">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="e9ee8-126">Se nessuna delle due interfaccia utente è disponibile, la funzione restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-126">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e9ee8-127">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-127">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="e9ee8-128">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-128">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="e9ee8-129">Specifica l'handle per la finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-129">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee8-130">**bstrFolderName**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-130">**bstrFolderName**</span></span>
</dt> <dd>

<span data-ttu-id="e9ee8-131">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-131">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="e9ee8-132">Specifica il nome della cartella in cui vengono trasferiti i file.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-132">Specifies the folder name where the files are transferred.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee8-133">**Bstrfilename**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-133">**bstrFilename**</span></span>
</dt> <dd>

<span data-ttu-id="e9ee8-134">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-134">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="e9ee8-135">Specifica il modello di nome file da utilizzare per i file trasferiti da elementi WIA alla cartella di destinazione designata da **bstrFolderName**.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-135">Specifies the filename template to be used for files transferred from WIA items to the destination folder designated by **bstrFolderName**.</span></span> <span data-ttu-id="e9ee8-136">È possibile creare un numero arbitrario di nomi di file univoci aggiungendo caratteri aggiuntivi al modello di nome file.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-136">An arbitrary number of unique file names can be created by appending additional characters to the file name template.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee8-137">**lNumFiles**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-137">**lNumFiles**</span></span>
</dt> <dd>

<span data-ttu-id="e9ee8-138">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-138">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="e9ee8-139">Riceve il numero di stringhe scritte nella matrice **pbstrFilePaths.**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-139">Receives the number of strings written to the **pbstrFilePaths** array.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee8-140">**pbstrFilePaths**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-140">**pbstrFilePaths**</span></span>
</dt> <dd>

<span data-ttu-id="e9ee8-141">Tipo: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="e9ee8-141">Type: **BSTR\***</span></span>

</dd> <dd>

<span data-ttu-id="e9ee8-142">Puntatore a una matrice di puntatori BSTR.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-142">Pointer to an array of BSTR pointers.</span></span> <span data-ttu-id="e9ee8-143">Ogni elemento della matrice punta a un BSTR che contiene il nome di destinazione di un file che è stato trasferito correttamente nella cartella identificata da bstrFolderName.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-143">Each array element points to a BSTR that contains the destination name of a file that was successfully transferred to the folder identified by bstrFolderName.</span></span> <span data-ttu-id="e9ee8-144">Il metodo deve allocare l'archiviazione per questo membro.</span><span class="sxs-lookup"><span data-stu-id="e9ee8-144">The method must allocate the storage for this member.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee8-145">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-145">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="e9ee8-146">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e9ee8-146">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="e9ee8-147">Puntatore [**all'interfaccia IWiaItem2**](-wia-iwiaitem2.md) dell'elemento WIA che trasferisce i dati al file o ai file denominati nella matrice **pbstrFilePaths.**</span><span class="sxs-lookup"><span data-stu-id="e9ee8-147">Pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the WIA item that transfers data to the file or files named in the **pbstrFilePaths** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9ee8-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9ee8-148">Requirements</span></span>



| <span data-ttu-id="e9ee8-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ee8-149">Requirement</span></span> | <span data-ttu-id="e9ee8-150">Valore</span><span class="sxs-lookup"><span data-stu-id="e9ee8-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ee8-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9ee8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ee8-152">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e9ee8-152">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e9ee8-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9ee8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ee8-154">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9ee8-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e9ee8-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9ee8-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ee8-156"><dt>Wiadefd.h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ee8-156"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




