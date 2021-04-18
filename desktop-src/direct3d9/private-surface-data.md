---
description: È possibile archiviare qualsiasi tipo di dati specifici dell'applicazione con una superficie. Una superficie che rappresenta una mappa in un gioco, ad esempio, potrebbe contenere informazioni sul terreno.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Dati della superficie privata (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304380"
---
# <a name="private-surface-data-direct3d-9"></a><span data-ttu-id="aafa6-104">Dati della superficie privata (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aafa6-104">Private Surface Data (Direct3D 9)</span></span>

<span data-ttu-id="aafa6-105">È possibile archiviare qualsiasi tipo di dati specifici dell'applicazione con una superficie.</span><span class="sxs-lookup"><span data-stu-id="aafa6-105">You can store any kind of application-specific data with a surface.</span></span> <span data-ttu-id="aafa6-106">Una superficie che rappresenta una mappa in un gioco, ad esempio, potrebbe contenere informazioni sul terreno.</span><span class="sxs-lookup"><span data-stu-id="aafa6-106">For example, a surface representing a map in a game might contain information about terrain.</span></span>

<span data-ttu-id="aafa6-107">Una superficie può avere più di un buffer di dati privato.</span><span class="sxs-lookup"><span data-stu-id="aafa6-107">A surface can have more than one private data buffer.</span></span> <span data-ttu-id="aafa6-108">Ogni buffer viene identificato da un GUID fornito quando si alleghino i dati alla superficie.</span><span class="sxs-lookup"><span data-stu-id="aafa6-108">Each buffer is identified by a GUID that you supply when attaching the data to the surface.</span></span>

<span data-ttu-id="aafa6-109">Per archiviare i dati della superficie privata, utilizzare SetPrivateData, passando un puntatore al buffer di origine, la dimensione dei dati e un GUID definito dall'applicazione per i dati.</span><span class="sxs-lookup"><span data-stu-id="aafa6-109">To store private surface data, use SetPrivateData, passing a pointer to the source buffer, the size of the data, and an application-defined GUID for the data.</span></span> <span data-ttu-id="aafa6-110">Facoltativamente, i dati di origine possono esistere sotto forma di oggetto COM; in questo caso, si passa un puntatore al puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'oggetto e si imposta il \_ flag D3DSPD IUNKNOWNPOINTER.</span><span class="sxs-lookup"><span data-stu-id="aafa6-110">Optionally, the source data can exist in the form of a COM object; in this case, you pass a pointer to the object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface pointer and you set the D3DSPD\_IUNKNOWNPOINTER flag.</span></span>

<span data-ttu-id="aafa6-111">SetPrivateData alloca un buffer interno per i dati e lo copia.</span><span class="sxs-lookup"><span data-stu-id="aafa6-111">SetPrivateData allocates an internal buffer for the data and copies it.</span></span> <span data-ttu-id="aafa6-112">È quindi possibile liberare in modo sicuro il buffer o l'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="aafa6-112">You can then safely free the source buffer or object.</span></span> <span data-ttu-id="aafa6-113">Il buffer interno o il riferimento all'interfaccia viene rilasciato quando viene chiamato FreePrivateData.</span><span class="sxs-lookup"><span data-stu-id="aafa6-113">The internal buffer or interface reference is released when FreePrivateData is called.</span></span> <span data-ttu-id="aafa6-114">Questa operazione viene eseguita automaticamente quando viene liberata la superficie.</span><span class="sxs-lookup"><span data-stu-id="aafa6-114">This happens automatically when the surface is freed.</span></span>

<span data-ttu-id="aafa6-115">Per recuperare i dati privati per una superficie, è necessario allocare un buffer con la dimensione corretta, quindi chiamare il metodo GetPrivateData, passando il GUID assegnato ai dati.</span><span class="sxs-lookup"><span data-stu-id="aafa6-115">To retrieve private data for a surface, you must allocate a buffer of the correct size and then call the GetPrivateData method, passing the GUID that was assigned to the data.</span></span> <span data-ttu-id="aafa6-116">L'utente è responsabile di liberare la memoria dinamica usata per questo buffer.</span><span class="sxs-lookup"><span data-stu-id="aafa6-116">You are responsible for freeing any dynamic memory you use for this buffer.</span></span> <span data-ttu-id="aafa6-117">Se i dati sono un oggetto COM, questo metodo recupera il puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aafa6-117">If the data is a COM object, this method retrieves the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="aafa6-118">Se non si conosce la dimensione di un buffer da allocare, chiamare prima GetPrivateData con zero in pSizeOfData.</span><span class="sxs-lookup"><span data-stu-id="aafa6-118">If you don't know how big a buffer to allocate, first call GetPrivateData with zero in pSizeOfData.</span></span> <span data-ttu-id="aafa6-119">Se il metodo ha esito negativo con D3DERR \_ MOREDATA, restituisce il numero di byte necessari per il buffer.</span><span class="sxs-lookup"><span data-stu-id="aafa6-119">If the method fails with D3DERR\_MOREDATA, it returns the necessary number of bytes for the buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aafa6-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aafa6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aafa6-121">Superfici Direct3D</span><span class="sxs-lookup"><span data-stu-id="aafa6-121">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 
