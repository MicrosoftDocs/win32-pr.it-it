---
description: In molte applicazioni le immagini vengono archiviate in modo permanente come file. Ad esempio, se si disegnano applicazioni, le immagini vengono archiviate in fogli di calcolo, i grafici e le applicazioni CAD e così via.
ms.assetid: fc43ab78-c174-400b-a73a-c346d8bda8d2
title: Archiviazione di un'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf47a869481d9ec7d71d594ddb238be14f9b152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529275"
---
# <a name="storing-an-image"></a><span data-ttu-id="27bb8-104">Archiviazione di un'immagine</span><span class="sxs-lookup"><span data-stu-id="27bb8-104">Storing an Image</span></span>

<span data-ttu-id="27bb8-105">In molte applicazioni le immagini vengono archiviate in modo permanente come file.</span><span class="sxs-lookup"><span data-stu-id="27bb8-105">Many applications store images permanently as files.</span></span> <span data-ttu-id="27bb8-106">Ad esempio, se si disegnano applicazioni, le immagini vengono archiviate in fogli di calcolo, i grafici e le applicazioni CAD e così via.</span><span class="sxs-lookup"><span data-stu-id="27bb8-106">For example, drawing applications store pictures, spreadsheet applications store charts, CAD applications store drawings, and so on.</span></span>

<span data-ttu-id="27bb8-107">Se si sta scrivendo un'applicazione che archivia un'immagine bitmap in un file, è necessario utilizzare il formato di file bitmap descritto nell' [Archivio bitmap](bitmap-storage.md).</span><span class="sxs-lookup"><span data-stu-id="27bb8-107">If you are writing an application that stores a bitmap image in a file, you should use the bitmap file format described in [Bitmap Storage](bitmap-storage.md).</span></span> <span data-ttu-id="27bb8-108">Per archiviare una bitmap in questo formato, è necessario usare una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)o [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) e una matrice di strutture [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , oltre a una matrice di indici della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="27bb8-108">To store a bitmap in this format, you must use a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), a [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header), or a [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure and an array of [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures, as well as an array of palette indexes.</span></span>

<span data-ttu-id="27bb8-109">Il codice di esempio seguente definisce una funzione che usa una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) e alloca memoria per e inizializza i membri all'interno di una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="27bb8-109">The following example code defines a function that uses a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure and allocates memory for and initializes members within a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure.</span></span> <span data-ttu-id="27bb8-110">Si noti che non è possibile usare la struttura **BITMAPINFO** con una struttura [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) o [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .</span><span class="sxs-lookup"><span data-stu-id="27bb8-110">Note that the **BITMAPINFO** structure cannot be used with either a [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) or a [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure.</span></span>


```C++
PBITMAPINFO CreateBitmapInfoStruct(HWND hwnd, HBITMAP hBmp)
{ 
    BITMAP bmp; 
    PBITMAPINFO pbmi; 
    WORD    cClrBits; 

    // Retrieve the bitmap color format, width, and height.  
    if (!GetObject(hBmp, sizeof(BITMAP), (LPSTR)&bmp)) 
        errhandler("GetObject", hwnd); 

    // Convert the color format to a count of bits.  
    cClrBits = (WORD)(bmp.bmPlanes * bmp.bmBitsPixel); 
    if (cClrBits == 1) 
        cClrBits = 1; 
    else if (cClrBits <= 4) 
        cClrBits = 4; 
    else if (cClrBits <= 8) 
        cClrBits = 8; 
    else if (cClrBits <= 16) 
        cClrBits = 16; 
    else if (cClrBits <= 24) 
        cClrBits = 24; 
    else cClrBits = 32; 

    // Allocate memory for the BITMAPINFO structure. (This structure  
    // contains a BITMAPINFOHEADER structure and an array of RGBQUAD  
    // data structures.)  

     if (cClrBits < 24) 
         pbmi = (PBITMAPINFO) LocalAlloc(LPTR, 
                    sizeof(BITMAPINFOHEADER) + 
                    sizeof(RGBQUAD) * (1<< cClrBits)); 

     // There is no RGBQUAD array for these formats: 24-bit-per-pixel or 32-bit-per-pixel 

     else 
         pbmi = (PBITMAPINFO) LocalAlloc(LPTR, 
                    sizeof(BITMAPINFOHEADER)); 

    // Initialize the fields in the BITMAPINFO structure.  

    pbmi->bmiHeader.biSize = sizeof(BITMAPINFOHEADER); 
    pbmi->bmiHeader.biWidth = bmp.bmWidth; 
    pbmi->bmiHeader.biHeight = bmp.bmHeight; 
    pbmi->bmiHeader.biPlanes = bmp.bmPlanes; 
    pbmi->bmiHeader.biBitCount = bmp.bmBitsPixel; 
    if (cClrBits < 24) 
        pbmi->bmiHeader.biClrUsed = (1<<cClrBits); 

    // If the bitmap is not compressed, set the BI_RGB flag.  
    pbmi->bmiHeader.biCompression = BI_RGB; 

    // Compute the number of bytes in the array of color  
    // indices and store the result in biSizeImage.  
    // The width must be DWORD aligned unless the bitmap is RLE 
    // compressed. 
    pbmi->bmiHeader.biSizeImage = ((pbmi->bmiHeader.biWidth * cClrBits +31) & ~31) /8
                                  * pbmi->bmiHeader.biHeight; 
    // Set biClrImportant to 0, indicating that all of the  
    // device colors are important.  
     pbmi->bmiHeader.biClrImportant = 0; 
     return pbmi; 
 } 
```



<span data-ttu-id="27bb8-111">Nell'esempio di codice seguente viene definita una funzione che Inizializza le strutture rimanenti, recupera la matrice degli indici della tavolozza, apre il file, copia i dati e chiude il file.</span><span class="sxs-lookup"><span data-stu-id="27bb8-111">The following example code defines a function that initializes the remaining structures, retrieves the array of palette indices, opens the file, copies the data, and closes the file.</span></span>


```C++
void CreateBMPFile(HWND hwnd, LPTSTR pszFile, PBITMAPINFO pbi, 
                  HBITMAP hBMP, HDC hDC) 
 { 
     HANDLE hf;                 // file handle  
    BITMAPFILEHEADER hdr;       // bitmap file-header  
    PBITMAPINFOHEADER pbih;     // bitmap info-header  
    LPBYTE lpBits;              // memory pointer  
    DWORD dwTotal;              // total count of bytes  
    DWORD cb;                   // incremental count of bytes  
    BYTE *hp;                   // byte pointer  
    DWORD dwTmp; 

    pbih = (PBITMAPINFOHEADER) pbi; 
    lpBits = (LPBYTE) GlobalAlloc(GMEM_FIXED, pbih->biSizeImage);

    if (!lpBits) 
         errhandler("GlobalAlloc", hwnd); 

    // Retrieve the color table (RGBQUAD array) and the bits  
    // (array of palette indices) from the DIB.  
    if (!GetDIBits(hDC, hBMP, 0, (WORD) pbih->biHeight, lpBits, pbi, 
        DIB_RGB_COLORS)) 
    {
        errhandler("GetDIBits", hwnd); 
    }

    // Create the .BMP file.  
    hf = CreateFile(pszFile, 
                   GENERIC_READ | GENERIC_WRITE, 
                   (DWORD) 0, 
                    NULL, 
                   CREATE_ALWAYS, 
                   FILE_ATTRIBUTE_NORMAL, 
                   (HANDLE) NULL); 
    if (hf == INVALID_HANDLE_VALUE) 
        errhandler("CreateFile", hwnd); 
    hdr.bfType = 0x4d42;        // 0x42 = "B" 0x4d = "M"  
    // Compute the size of the entire file.  
    hdr.bfSize = (DWORD) (sizeof(BITMAPFILEHEADER) + 
                 pbih->biSize + pbih->biClrUsed 
                 * sizeof(RGBQUAD) + pbih->biSizeImage); 
    hdr.bfReserved1 = 0; 
    hdr.bfReserved2 = 0; 

    // Compute the offset to the array of color indices.  
    hdr.bfOffBits = (DWORD) sizeof(BITMAPFILEHEADER) + 
                    pbih->biSize + pbih->biClrUsed 
                    * sizeof (RGBQUAD); 

    // Copy the BITMAPFILEHEADER into the .BMP file.  
    if (!WriteFile(hf, (LPVOID) &hdr, sizeof(BITMAPFILEHEADER), 
        (LPDWORD) &dwTmp,  NULL)) 
    {
       errhandler("WriteFile", hwnd); 
    }

    // Copy the BITMAPINFOHEADER and RGBQUAD array into the file.  
    if (!WriteFile(hf, (LPVOID) pbih, sizeof(BITMAPINFOHEADER) 
                  + pbih->biClrUsed * sizeof (RGBQUAD), 
                  (LPDWORD) &dwTmp, ( NULL)))
        errhandler("WriteFile", hwnd); 

    // Copy the array of color indices into the .BMP file.  
    dwTotal = cb = pbih->biSizeImage; 
    hp = lpBits; 
    if (!WriteFile(hf, (LPSTR) hp, (int) cb, (LPDWORD) &dwTmp,NULL)) 
           errhandler("WriteFile", hwnd); 

    // Close the .BMP file.  
     if (!CloseHandle(hf)) 
           errhandler("CloseHandle", hwnd); 

    // Free memory.  
    GlobalFree((HGLOBAL)lpBits);
}
```



 

 
