---
title: Trasformazione di un'immagine JPEG senza perdita di dati
description: Quando si comprime un'immagine JPEG, alcune informazioni nell'immagine vengono perse.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ea7011f25a97a228c44bdb87ba09ca8b284ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977543"
---
# <a name="lossless-transform-of-a-jpeg-image"></a><span data-ttu-id="4d73b-103">Trasformazione di un'immagine JPEG senza perdita di dati</span><span class="sxs-lookup"><span data-stu-id="4d73b-103">Lossless transform of a JPEG image</span></span>

<span data-ttu-id="4d73b-104">Quando si comprime un'immagine JPEG, alcune informazioni nell'immagine vengono perse.</span><span class="sxs-lookup"><span data-stu-id="4d73b-104">When you compress a JPEG image, some of the information in the image is lost.</span></span> <span data-ttu-id="4d73b-105">Se si apre un file JPEG, si modifica l'immagine e lo si salva in un altro file JPEG, la qualità diminuisce.</span><span class="sxs-lookup"><span data-stu-id="4d73b-105">If you open a JPEG file, alter the image, and save it to another JPEG file, the quality will decrease.</span></span> <span data-ttu-id="4d73b-106">Se si ripete il processo più volte, si noterà un calo sostanziale della qualità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="4d73b-106">If you repeat that process many times, you will see a substantial degradation in the image quality.</span></span>

<span data-ttu-id="4d73b-107">Poiché il formato JPEG è uno dei formati di immagine più diffusi sul Web e, poiché spesso si desidera modificare le immagini JPEG, GDI+ fornisce le trasformazioni seguenti che possono essere eseguite sulle immagini JPEG senza perdita di informazioni:</span><span class="sxs-lookup"><span data-stu-id="4d73b-107">Because JPEG is one of the most popular image formats on the Web, and because people often like to modify JPEG images, GDI+ provides the following transformations that can be performed on JPEG images without loss of information:</span></span>

-   <span data-ttu-id="4d73b-108">Ruota di 90 gradi</span><span class="sxs-lookup"><span data-stu-id="4d73b-108">Rotate 90 degrees</span></span>
-   <span data-ttu-id="4d73b-109">Ruota di 180 gradi</span><span class="sxs-lookup"><span data-stu-id="4d73b-109">Rotate 180 degrees</span></span>
-   <span data-ttu-id="4d73b-110">Ruota di 270 gradi</span><span class="sxs-lookup"><span data-stu-id="4d73b-110">Rotate 270 degrees</span></span>
-   <span data-ttu-id="4d73b-111">Capovolgi orizzontalmente</span><span class="sxs-lookup"><span data-stu-id="4d73b-111">Flip horizontally</span></span>
-   <span data-ttu-id="4d73b-112">Capovolgi verticalmente</span><span class="sxs-lookup"><span data-stu-id="4d73b-112">Flip vertically</span></span>

<span data-ttu-id="4d73b-113">È possibile applicare una delle trasformazioni mostrate nell'elenco precedente quando si chiama il metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) di un oggetto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="4d73b-113">You can apply one of the transformations shown in the preceding list when you call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="4d73b-114">Se vengono soddisfatte le condizioni seguenti, la trasformazione proseguirà senza perdita di informazioni:</span><span class="sxs-lookup"><span data-stu-id="4d73b-114">If the following conditions are met, then the transformation will proceed without loss of information:</span></span>

-   <span data-ttu-id="4d73b-115">Il file usato per costruire l'oggetto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) è un file JPEG.</span><span class="sxs-lookup"><span data-stu-id="4d73b-115">The file used to construct the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object is a JPEG file.</span></span>
-   <span data-ttu-id="4d73b-116">La larghezza e l'altezza dell'immagine sono entrambi multipli di 16.</span><span class="sxs-lookup"><span data-stu-id="4d73b-116">The width and height of the image are both multiples of 16.</span></span>

<span data-ttu-id="4d73b-117">Se la larghezza e l'altezza dell'immagine non sono entrambi multipli di 16, GDI+ ne eseguirà la migliore per mantenere la qualità dell'immagine quando si applica una delle trasformazioni di rotazione o capovolgimento visualizzate nell'elenco precedente.</span><span class="sxs-lookup"><span data-stu-id="4d73b-117">If the width and height of the image are not both multiples of 16, GDI+ will do its best to preserve the image quality when you apply one of the rotation or flipping transformations shown in the preceding list.</span></span>

<span data-ttu-id="4d73b-118">Per trasformare un'immagine JPEG, inizializzare un oggetto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) e passare l'indirizzo dell'oggetto al metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) della classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="4d73b-118">To transform a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="4d73b-119">Inizializzare l'oggetto **EncoderParameters** in modo che disponga di una matrice costituita da un oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="4d73b-119">Initialize the **EncoderParameters** object so that it has an array that consists of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="4d73b-120">Inizializzare un oggetto **EncoderParameter** in modo che il membro **value** punti a una variabile **ULONG** che include uno degli elementi seguenti dell'enumerazione [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :</span><span class="sxs-lookup"><span data-stu-id="4d73b-120">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** variable that holds one of the following elements of the [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>

-   <span data-ttu-id="4d73b-121">EncoderValueTransformRotate90,</span><span class="sxs-lookup"><span data-stu-id="4d73b-121">EncoderValueTransformRotate90,</span></span>
-   <span data-ttu-id="4d73b-122">EncoderValueTransformRotate180,</span><span class="sxs-lookup"><span data-stu-id="4d73b-122">EncoderValueTransformRotate180,</span></span>
-   <span data-ttu-id="4d73b-123">EncoderValueTransformRotate270,</span><span class="sxs-lookup"><span data-stu-id="4d73b-123">EncoderValueTransformRotate270,</span></span>
-   <span data-ttu-id="4d73b-124">EncoderValueTransformFlipHorizontal,</span><span class="sxs-lookup"><span data-stu-id="4d73b-124">EncoderValueTransformFlipHorizontal,</span></span>
-   <span data-ttu-id="4d73b-125">EncoderValueTransformFlipVertical</span><span class="sxs-lookup"><span data-stu-id="4d73b-125">EncoderValueTransformFlipVertical</span></span>

<span data-ttu-id="4d73b-126">Impostare il membro **GUID** dell'oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) su EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="4d73b-126">Set the **Guid** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object to EncoderTransformation.</span></span>

<span data-ttu-id="4d73b-127">La seguente applicazione console crea un oggetto [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) da un file JPEG e quindi Salva l'immagine in un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="4d73b-127">The following console application creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then saves the image to a new file.</span></span> <span data-ttu-id="4d73b-128">Durante il processo di salvataggio, l'immagine viene ruotata di 90 gradi.</span><span class="sxs-lookup"><span data-stu-id="4d73b-128">During the save process, the image is rotated 90 degrees.</span></span> <span data-ttu-id="4d73b-129">Se la larghezza e l'altezza dell'immagine sono entrambi multipli di 16, il processo di rotazione e salvataggio dell'immagine non comporta la perdita di informazioni.</span><span class="sxs-lookup"><span data-stu-id="4d73b-129">If the width and height of the image are both multiples of 16, the process of rotating and saving the image causes no loss of information.</span></span>

<span data-ttu-id="4d73b-130">La funzione Main si basa sulla funzione helper GetEncoderClsid, che viene mostrata durante il [recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="4d73b-130">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID             encoderClsid;
   EncoderParameters encoderParameters;
   ULONG             transformation;
   UINT              width;
   UINT              height;
   Status            stat;

   // Get a JPEG image from the disk.
   Image* image = new Image(L"Shapes.jpg");

   // Determine whether the width and height of the image 
   // are multiples of 16.
   width = image->GetWidth();
   height = image->GetHeight();

   printf("The width of the image is %u", width);
   if(width / 16.0 - width / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   printf("The height of the image is %u", height);
   if(height / 16.0 - height / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will set that value to EncoderValueTransformRotate90.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderTransformation;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Rotate and save the image.
   transformation = EncoderValueTransformRotate90;
   encoderParameters.Parameter[0].Value = &transformation;
   stat = image->Save(L"ShapesR90.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"ShapesR90.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"ShapesR90.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
