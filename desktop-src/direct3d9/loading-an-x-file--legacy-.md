---
description: Per caricare un file con estensione x, attenersi alla procedura seguente in applicazioni legacy.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Caricamento di un file X (legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521169"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a><span data-ttu-id="79c19-103">Caricamento di un file X (legacy) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="79c19-103">Loading an X File (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="79c19-104">Per caricare un file con estensione x, attenersi alla procedura seguente in applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="79c19-104">Use the following procedure in legacy applications to load a .x file.</span></span>

1.  <span data-ttu-id="79c19-105">Usare la funzione [**DirectXFileCreate**](directxfilecreate.md) per creare un oggetto [**IDirectXFile**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="79c19-105">Use the [**DirectXFileCreate**](directxfilecreate.md) function to create an [**IDirectXFile**](idirectxfile.md) object.</span></span>
2.  <span data-ttu-id="79c19-106">Se i modelli sono presenti nel file DirectX che verrà caricato, usare il metodo [**IDirectXFile:: RegisterTemplates**](idirectxfile--registertemplates.md) per registrare tali modelli.</span><span class="sxs-lookup"><span data-stu-id="79c19-106">If templates are present in the DirectX file that you will load, use the [**IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) method to register those templates.</span></span>
3.  <span data-ttu-id="79c19-107">Usare il metodo [**IDirectXFile:: CreateEnumObject**](idirectxfile--createenumobject.md) per creare un oggetto enumeratore [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="79c19-107">Use the [**IDirectXFile::CreateEnumObject**](idirectxfile--createenumobject.md) method to create an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) enumerator object.</span></span>
4.  <span data-ttu-id="79c19-108">Scorrere gli oggetti nel file.</span><span class="sxs-lookup"><span data-stu-id="79c19-108">Loop through the objects in the file.</span></span> <span data-ttu-id="79c19-109">Per ogni oggetto, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="79c19-109">For each object, perform the following steps.</span></span>
    1.  <span data-ttu-id="79c19-110">Usare il metodo [**IDirectXFileEnumObject:: GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) per recuperare ciascun oggetto [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="79c19-110">Use the [**IDirectXFileEnumObject::GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) method to retrieve each [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
    2.  <span data-ttu-id="79c19-111">Usare il metodo [**IDirectXFileData:: GetType**](idirectxfiledata--gettype.md) per recuperare il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="79c19-111">Use the [**IDirectXFileData::GetType**](idirectxfiledata--gettype.md) method to retrieve the data's type.</span></span>
    3.  <span data-ttu-id="79c19-112">Caricare i dati usando il metodo [**IDirectXFileData:: GetData**](idirectxfiledata--getdata.md) .</span><span class="sxs-lookup"><span data-stu-id="79c19-112">Load the data using the [**IDirectXFileData::GetData**](idirectxfiledata--getdata.md) method.</span></span>
    4.  <span data-ttu-id="79c19-113">Se l'oggetto dispone di membri facoltativi, recuperare i membri facoltativi chiamando il metodo [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) .</span><span class="sxs-lookup"><span data-stu-id="79c19-113">If the object has optional members, retrieve the optional members by calling the [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) method.</span></span>
    5.  <span data-ttu-id="79c19-114">Rilasciare l'oggetto [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="79c19-114">Release the [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
5.  <span data-ttu-id="79c19-115">Rilasciare l'oggetto [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="79c19-115">Release the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) object.</span></span>
6.  <span data-ttu-id="79c19-116">Rilasciare l'oggetto [**IDirectXFile**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="79c19-116">Release the [**IDirectXFile**](idirectxfile.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79c19-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79c19-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79c19-118">File X (legacy)</span><span class="sxs-lookup"><span data-stu-id="79c19-118">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



