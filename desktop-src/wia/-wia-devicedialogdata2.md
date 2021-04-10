---
description: Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Struttura DEVICEDIALOGDATA2 (Wiadefd. h)
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
ms.openlocfilehash: f4ab56114054b4f69a21fd9f4c05a1e119bab5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050039"
---
# <a name="devicedialogdata2-structure"></a><span data-ttu-id="d8b0a-103">Struttura DEVICEDIALOGDATA2</span><span class="sxs-lookup"><span data-stu-id="d8b0a-103">DEVICEDIALOGDATA2 structure</span></span>

<span data-ttu-id="d8b0a-104">Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b0a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8b0a-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="d8b0a-106">Members</span><span class="sxs-lookup"><span data-stu-id="d8b0a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8b0a-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d8b0a-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8b0a-109">Specifica la dimensione in byte della struttura.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d8b0a-110">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-110">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="d8b0a-111">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d8b0a-111">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

</dd> <dd>

<span data-ttu-id="d8b0a-112">Punta a un'interfaccia [_ *IWiaItem2* \*](-wia-iwiaitem2.md) che rappresenta l'elemento radice valido nell'albero degli elementi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-112">Points to an [_ *IWiaItem2*\*](-wia-iwiaitem2.md) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="d8b0a-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d8b0a-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8b0a-115">Specifica un set di flag che controllano l'operazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-115">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="d8b0a-116">Può essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8b0a-116">Can be set to any of the following values:</span></span>



| <span data-ttu-id="d8b0a-117">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="d8b0a-117">Flag</span></span>                                 | <span data-ttu-id="d8b0a-118">Significato</span><span class="sxs-lookup"><span data-stu-id="d8b0a-118">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b0a-119">0</span><span class="sxs-lookup"><span data-stu-id="d8b0a-119">0</span></span>                                    | <span data-ttu-id="d8b0a-120">Comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-120">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="d8b0a-121">\_ \_ immagine singola della finestra di dialogo del dispositivo WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="d8b0a-121">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="d8b0a-122">Limitare la selezione delle immagini a una singola immagine nella finestra di dialogo acquisizione immagine del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-122">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="d8b0a-123">\_finestra di dialogo del dispositivo WIA usare l' \_ \_ \_ \_ interfaccia utente comune</span><span class="sxs-lookup"><span data-stu-id="d8b0a-123">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="d8b0a-124">Utilizzare l'interfaccia utente di sistema, se disponibile, anziché l'interfaccia utente fornita dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-124">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="d8b0a-125">Se l'interfaccia utente del sistema non è disponibile, viene utilizzata l'interfaccia utente del fornitore.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-125">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="d8b0a-126">Se nessuna delle due interfacce è disponibile, la funzione restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-126">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d8b0a-127">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-127">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="d8b0a-128">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-128">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="d8b0a-129">Specifica l'handle per la finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-129">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="d8b0a-130">**bstrFolderName**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-130">**bstrFolderName**</span></span>
</dt> <dd>

<span data-ttu-id="d8b0a-131">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-131">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d8b0a-132">Specifica il nome della cartella in cui vengono trasferiti i file.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-132">Specifies the folder name where the files are transferred.</span></span>

</dd> <dt>

<span data-ttu-id="d8b0a-133">**bstrFilename**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-133">**bstrFilename**</span></span>
</dt> <dd>

<span data-ttu-id="d8b0a-134">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-134">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d8b0a-135">Specifica il modello di nome file da utilizzare per i file trasferiti dagli elementi WIA alla cartella di destinazione indicata da **bstrFolderName**.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-135">Specifies the filename template to be used for files transferred from WIA items to the destination folder designated by **bstrFolderName**.</span></span> <span data-ttu-id="d8b0a-136">È possibile creare un numero arbitrario di nomi file univoci aggiungendo caratteri aggiuntivi al modello di nome file.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-136">An arbitrary number of unique file names can be created by appending additional characters to the file name template.</span></span>

</dd> <dt>

<span data-ttu-id="d8b0a-137">**lNumFiles**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-137">**lNumFiles**</span></span>
</dt> <dd>

<span data-ttu-id="d8b0a-138">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-138">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="d8b0a-139">Riceve il numero di stringhe scritte nella matrice **pbstrFilePaths** .</span><span class="sxs-lookup"><span data-stu-id="d8b0a-139">Receives the number of strings written to the **pbstrFilePaths** array.</span></span>

</dd> <dt>

<span data-ttu-id="d8b0a-140">**pbstrFilePaths**</span><span class="sxs-lookup"><span data-stu-id="d8b0a-140">**pbstrFilePaths**</span></span>
</dt> <dd>

<span data-ttu-id="d8b0a-141">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="d8b0a-141">Type: \**BSTR\** _</span></span>

</dd> <dd>

<span data-ttu-id="d8b0a-142">Puntatore a una matrice di puntatori BSTR.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-142">Pointer to an array of BSTR pointers.</span></span> <span data-ttu-id="d8b0a-143">Ogni elemento della matrice punta a un BSTR che contiene il nome di destinazione di un file che è stato trasferito correttamente nella cartella identificata da bstrFolderName.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-143">Each array element points to a BSTR that contains the destination name of a file that was successfully transferred to the folder identified by bstrFolderName.</span></span> <span data-ttu-id="d8b0a-144">Il metodo deve allocare lo spazio di archiviazione per il membro.</span><span class="sxs-lookup"><span data-stu-id="d8b0a-144">The method must allocate the storage for this member.</span></span>

</dd> <dt>

<span data-ttu-id="d8b0a-145">_ *ppWiaItem*\*</span><span class="sxs-lookup"><span data-stu-id="d8b0a-145">_ *ppWiaItem*\*</span></span>
</dt> <dd>

<span data-ttu-id="d8b0a-146">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d8b0a-146">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

</dd> <dd>

<span data-ttu-id="d8b0a-147">Puntatore all'interfaccia [_ *IWiaItem2* \*](-wia-iwiaitem2.md) dell'elemento WIA che trasferisce i dati al file o ai file denominati nella matrice **pbstrFilePaths** .</span><span class="sxs-lookup"><span data-stu-id="d8b0a-147">Pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) interface of the WIA item that transfers data to the file or files named in the **pbstrFilePaths** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8b0a-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8b0a-148">Requirements</span></span>



| <span data-ttu-id="d8b0a-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8b0a-149">Requirement</span></span> | <span data-ttu-id="d8b0a-150">Valore</span><span class="sxs-lookup"><span data-stu-id="d8b0a-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b0a-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8b0a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b0a-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8b0a-152">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d8b0a-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8b0a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b0a-154">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8b0a-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d8b0a-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8b0a-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8b0a-156"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b0a-156"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




