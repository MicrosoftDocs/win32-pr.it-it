---
description: CPersistStream è la classe base per le proprietà permanenti dei filtri, ovvero le proprietà di filtro nei grafici salvati.
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: Classe CPersistStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520785"
---
# <a name="cpersiststream-class"></a><span data-ttu-id="df901-103">Classe CPersistStream</span><span class="sxs-lookup"><span data-stu-id="df901-103">CPersistStream class</span></span>

![gerarchia di classi cpersiststream](images/pstrm01.png)

<span data-ttu-id="df901-105">`CPersistStream` è la classe base per le proprietà permanenti dei filtri, ovvero le proprietà di filtro nei grafici salvati.</span><span class="sxs-lookup"><span data-stu-id="df901-105">`CPersistStream` is the base class for persistent properties of filters (that is, filter properties in saved graphs).</span></span>

<span data-ttu-id="df901-106">Il modo più semplice per usare `CPersistStream` è:</span><span class="sxs-lookup"><span data-stu-id="df901-106">The simplest way to use `CPersistStream` is to:</span></span>

1.  <span data-ttu-id="df901-107">Disporre che il filtro erediti questa classe.</span><span class="sxs-lookup"><span data-stu-id="df901-107">Arrange for your filter to inherit this class.</span></span>
2.  <span data-ttu-id="df901-108">Implementare [**WriteToStream**](cpersiststream-writetostream.md) e [**ReadFromStream**](cpersiststream-readfromstream.md) nella classe.</span><span class="sxs-lookup"><span data-stu-id="df901-108">Implement [**WriteToStream**](cpersiststream-writetostream.md) and [**ReadFromStream**](cpersiststream-readfromstream.md) in your class.</span></span> <span data-ttu-id="df901-109">Queste funzioni eseguiranno l'override delle funzioni, che non eseguono alcuna operazione, ma fungono da segnaposto.</span><span class="sxs-lookup"><span data-stu-id="df901-109">These will override the functions here, which do nothing but act as placeholders.</span></span>
3.  <span data-ttu-id="df901-110">Modificare il **NonDelegatingQueryInterface** per gestire **IPersistStream**.</span><span class="sxs-lookup"><span data-stu-id="df901-110">Change your **NonDelegatingQueryInterface** to handle **IPersistStream**.</span></span>
4.  <span data-ttu-id="df901-111">Implementare [**SizeMax**](cpersiststream-sizemax.md) per restituire un limite superiore per il numero di byte di dati salvati.</span><span class="sxs-lookup"><span data-stu-id="df901-111">Implement [**SizeMax**](cpersiststream-sizemax.md) to return an upper bound on the number of bytes of data you save.</span></span>

    <span data-ttu-id="df901-112">Se si salvano i dati™ Unicode, tenere presente che WCHAR è di 2 byte.</span><span class="sxs-lookup"><span data-stu-id="df901-112">If you save Unicode™ data, remember that a WCHAR is 2 bytes.</span></span>

5.  <span data-ttu-id="df901-113">Quando i dati vengono modificati, chiamare [**sedirty**](cpersiststream-setdirty.md).</span><span class="sxs-lookup"><span data-stu-id="df901-113">When your data changes, call [**SetDirty**](cpersiststream-setdirty.md).</span></span>

## <a name="version-numbers"></a><span data-ttu-id="df901-114">Numeri di versione</span><span class="sxs-lookup"><span data-stu-id="df901-114">Version Numbers</span></span>

<span data-ttu-id="df901-115">A un certo punto è possibile decidere di modificare o estendere il formato dei dati.</span><span class="sxs-lookup"><span data-stu-id="df901-115">At some point you might decide to alter or extend the format of your data.</span></span> <span data-ttu-id="df901-116">Si desidera quindi avere un numero di versione in tutti i flussi salvati precedenti, in modo da poter indicare, quando vengono letti, se rappresentano il form precedente o nuovo.</span><span class="sxs-lookup"><span data-stu-id="df901-116">You will then wish you had a version number in all the old saved streams so you can tell, when you read them, whether they represent the old or new form.</span></span> <span data-ttu-id="df901-117">Per semplificare questa operazione, questa classe scrive e legge un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="df901-117">To assist you, this class writes and reads a version number.</span></span> <span data-ttu-id="df901-118">Quando scrive, viene chiamato [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) per richiedere la versione del software in uso al momento.</span><span class="sxs-lookup"><span data-stu-id="df901-118">When it writes, it calls [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) to inquire as to the version of the software being used at the moment.</span></span> <span data-ttu-id="df901-119">(In effetti, si tratta di un numero di versione del layout dei dati nel file). Scrive come prima cosa nei dati.</span><span class="sxs-lookup"><span data-stu-id="df901-119">(In effect, this is a version number of the data layout in the file.) It writes this as the first thing in the data.</span></span> <span data-ttu-id="df901-120">Se si desidera modificare la versione, implementare (override) **GetSoftwareVersion**.</span><span class="sxs-lookup"><span data-stu-id="df901-120">If you want to change the version, implement (override) **GetSoftwareVersion**.</span></span> <span data-ttu-id="df901-121">Il numero di versione viene letto dal file in **MP \_ dwFileVersion** prima di chiamare [**ReadFromStream**](cpersiststream-readfromstream.md), quindi in **ReadFromStream** è possibile controllare **mPS \_ dwFileVersion** per verificare se si sta leggendo un file di versione precedente.</span><span class="sxs-lookup"><span data-stu-id="df901-121">It reads the version number from the file into **mPS\_dwFileVersion** before calling [**ReadFromStream**](cpersiststream-readfromstream.md), so in **ReadFromStream** you can check **mPS\_dwFileVersion** to see if you are reading an old version file.</span></span> <span data-ttu-id="df901-122">In genere è necessario accettare i file la cui versione non è più recente rispetto alla versione del software che li sta leggendo.</span><span class="sxs-lookup"><span data-stu-id="df901-122">Usually you should accept files whose version is no newer than the software version that is reading them.</span></span>

<span data-ttu-id="df901-123">**CPersistStream** implementa [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="df901-123">**CPersistStream** implements [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="df901-124">Per ulteriori informazioni sull'implementazione, vedere la Guida di riferimento a COM in Microsoft Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="df901-124">For more implementation information, see the COM Reference in the Microsoft Platform SDK.</span></span>



| <span data-ttu-id="df901-125">Membri dati protetti</span><span class="sxs-lookup"><span data-stu-id="df901-125">Protected Data Members</span></span>                                          | <span data-ttu-id="df901-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df901-126">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="df901-127">\_DwFileVersion mPS</span><span class="sxs-lookup"><span data-stu-id="df901-127">mPS\_dwFileVersion</span></span>                                              | <span data-ttu-id="df901-128">Numero di versione del file.</span><span class="sxs-lookup"><span data-stu-id="df901-128">Version number of the file.</span></span>                                                   |
| <span data-ttu-id="df901-129">\_FDirty mPS</span><span class="sxs-lookup"><span data-stu-id="df901-129">mPS\_fDirty</span></span>                                                     | <span data-ttu-id="df901-130">I dati per questo flusso devono essere salvati.</span><span class="sxs-lookup"><span data-stu-id="df901-130">Data for this stream must be saved.</span></span>                                           |
| <span data-ttu-id="df901-131">Funzioni di membro</span><span class="sxs-lookup"><span data-stu-id="df901-131">Member Functions</span></span>                                                | <span data-ttu-id="df901-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df901-132">Description</span></span>                                                                   |
| [<span data-ttu-id="df901-133">**CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="df901-133">**CPersistStream**</span></span>](cpersiststream-cpersiststream.md)         | <span data-ttu-id="df901-134">Costruisce un oggetto **CPersistStream** .</span><span class="sxs-lookup"><span data-stu-id="df901-134">Constructs a **CPersistStream** object.</span></span>                                       |
| [<span data-ttu-id="df901-135">**SetDirty**</span><span class="sxs-lookup"><span data-stu-id="df901-135">**SetDirty**</span></span>](cpersiststream-setdirty.md)                     | <span data-ttu-id="df901-136">Indica che l'oggetto deve essere salvato nel flusso.</span><span class="sxs-lookup"><span data-stu-id="df901-136">Indicates that the object must be saved to the stream.</span></span>                        |
| <span data-ttu-id="df901-137">Funzioni membro sottoponibili a override</span><span class="sxs-lookup"><span data-stu-id="df901-137">Overridable Member Functions</span></span>                                    | <span data-ttu-id="df901-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df901-138">Description</span></span>                                                                   |
| [<span data-ttu-id="df901-139">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="df901-139">**GetClassID**</span></span>](cpersiststream-getclassid.md)                 | <span data-ttu-id="df901-140">Recupera l'identificatore di classe di questo flusso.</span><span class="sxs-lookup"><span data-stu-id="df901-140">Retrieves the class identifier of this stream.</span></span>                                |
| [<span data-ttu-id="df901-141">**GetSoftwareVersion**</span><span class="sxs-lookup"><span data-stu-id="df901-141">**GetSoftwareVersion**</span></span>](cpersiststream-getsoftwareversion.md) | <span data-ttu-id="df901-142">Recupera il numero di versione per questo formato di file.</span><span class="sxs-lookup"><span data-stu-id="df901-142">Retrieves the version number for this file format.</span></span>                            |
| [<span data-ttu-id="df901-143">**ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="df901-143">**ReadFromStream**</span></span>](cpersiststream-readfromstream.md)         | <span data-ttu-id="df901-144">Legge i dati del filtro dal flusso.</span><span class="sxs-lookup"><span data-stu-id="df901-144">Reads the filter's data from the stream.</span></span>                                      |
| [<span data-ttu-id="df901-145">**SizeMax**</span><span class="sxs-lookup"><span data-stu-id="df901-145">**SizeMax**</span></span>](cpersiststream-sizemax.md)                       | <span data-ttu-id="df901-146">Recupera il numero di byte necessari per i dati, escluso il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="df901-146">Retrieves the number of bytes needed for data (not including version number).</span></span> |
| [<span data-ttu-id="df901-147">**WriteToStream**</span><span class="sxs-lookup"><span data-stu-id="df901-147">**WriteToStream**</span></span>](cpersiststream-writetostream.md)           | <span data-ttu-id="df901-148">Scrive i dati del filtro nel flusso.</span><span class="sxs-lookup"><span data-stu-id="df901-148">Writes the filter's data to the stream.</span></span>                                       |
| <span data-ttu-id="df901-149">Metodi IPersistStream</span><span class="sxs-lookup"><span data-stu-id="df901-149">IPersistStream Methods</span></span>                                          | <span data-ttu-id="df901-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df901-150">Description</span></span>                                                                   |
| [<span data-ttu-id="df901-151">**GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="df901-151">**GetSizeMax**</span></span>](cpersiststream-getsizemax.md)                 | <span data-ttu-id="df901-152">Recupera il numero di byte necessari per i dati (incluso il numero di versione).</span><span class="sxs-lookup"><span data-stu-id="df901-152">Retrieves the number of bytes needed for data (including version number).</span></span>     |
| [<span data-ttu-id="df901-153">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="df901-153">**IsDirty**</span></span>](cpersiststream-isdirty.md)                       | <span data-ttu-id="df901-154">Controlla se l'oggetto deve essere salvato.</span><span class="sxs-lookup"><span data-stu-id="df901-154">Checks if the object must be saved.</span></span>                                           |
| [<span data-ttu-id="df901-155">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="df901-155">**Load**</span></span>](cpersiststream-load.md)                             | <span data-ttu-id="df901-156">Carica i dati dal flusso in memoria.</span><span class="sxs-lookup"><span data-stu-id="df901-156">Loads the data from the stream into memory.</span></span>                                   |
| [<span data-ttu-id="df901-157">**Salva**</span><span class="sxs-lookup"><span data-stu-id="df901-157">**Save**</span></span>](cpersiststream-save.md)                             | <span data-ttu-id="df901-158">Salva i dati dalla memoria al flusso.</span><span class="sxs-lookup"><span data-stu-id="df901-158">Saves the data from memory to the stream.</span></span>                                     |



 

 

 
