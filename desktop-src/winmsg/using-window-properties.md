---
description: In questa sezione viene illustrato come eseguire le attività seguenti associate alle proprietà della finestra.
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: Uso delle proprietà della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 736682eb34191a061aa9753ef9d5e8c7e366fbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312490"
---
# <a name="using-window-properties"></a>Uso delle proprietà della finestra

In questa sezione viene illustrato come eseguire le attività seguenti associate alle proprietà della finestra.

-   [Aggiunta di una proprietà della finestra](#adding-a-window-property)
-   [Recupero di una proprietà della finestra](#retrieving-a-window-property)
-   [Elenco delle proprietà della finestra per una determinata finestra](#listing-window-properties-for-a-given-window)
-   [Eliminazione di una proprietà di finestra](#deleting-a-window-property)

## <a name="adding-a-window-property"></a>Aggiunta di una proprietà della finestra

Nell'esempio seguente vengono caricati un'icona e quindi un cursore e viene allocata memoria per un buffer. Nell'esempio viene quindi utilizzata la funzione [**seprop**](/windows/win32/api/winuser/nf-winuser-setpropa) per assegnare l'icona, il cursore e gli handle di memoria risultanti come proprietà della finestra identificata dalla variabile hwndSubclass definita dall'applicazione. Le proprietà sono identificate dall'icona della PROP delle stringhe \_ , dal \_ cursore prop e dal buffer Prop \_ .


```
#define BUFFER 4096 
 
HINSTANCE hinst;       // handle of current instance 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIcon, hCursor; 
HGLOBAL hMem; 
char *lpMem; 
TCHAR tchPath[] = "c:\\winnt\\samples\\winprop.c";
HRESULT hResult; 
 
// Load resources. 
 
hIcon = LoadIcon(hinst, MAKEINTRESOURCE(400)); 
hCursor = LoadCursor(hinst, MAKEINTRESOURCE(220)); 
 
// Allocate and fill a memory buffer. 
 
hMem = GlobalAlloc(GPTR, BUFFER); 
lpMem = GlobalLock(hMem);
if (lpMem == NULL)
{
// TODO: write error handler
}
hResult = StringCchCopy(lpMem, STRSAFE_MAX_CCH, tchPath);
if (FAILED(hResult))
{
// TO DO: write error handler if function fails.
} 
GlobalUnlock(hMem); 
 
// Set the window properties for hwndSubclass. 
 
SetProp(hwndSubclass, "PROP_ICON", hIcon); 
SetProp(hwndSubclass, "PROP_CURSOR", hCursor); 
SetProp(hwndSubclass, "PROP_BUFFER", hMem); 
```



## <a name="retrieving-a-window-property"></a>Recupero di una proprietà della finestra

Una finestra può creare handle per i dati della proprietà della finestra e utilizzare i dati per qualsiasi scopo. Nell'esempio seguente viene usato [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) per ottenere handle per le proprietà della finestra identificate dall' \_ icona prop, dal cursore prop e dal \_ \_ buffer prop. Nell'esempio viene quindi visualizzato il contenuto del buffer di memoria, del cursore e dell'icona appena ottenuti nell'area client della finestra.


```
#define PATHLENGTH 256 
 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIconProp, hCursProp; 
HGLOBAL hMemProp; 
char *lpFilename; 
TCHAR tchBuffer[PATHLENGTH]; 
size_t * nSize; 
HDC hdc;
HRESULT hResult; 
 
// Get the window properties, then use the data. 
 
hIconProp = (HICON) GetProp(hwndSubclass, "PROP_ICON"); 
TextOut(hdc, 10, 40, "PROP_ICON", 9); 
DrawIcon(hdc, 90, 40, hIconProp); 
 
hCursProp = (HCURSOR) GetProp(hwndSubclass, "PROP_CURSOR"); 
TextOut(hdc, 10, 85, "PROP_CURSOR", 9); 
DrawIcon(hdc, 110, 85, hCursProp); 
 
hMemProp = (HGLOBAL) GetProp(hwndSubclass, "PROP_BUFFER"); 
lpFilename = GlobalLock(hMemProp);
hResult = StringCchPrintf(tchBuffer, PATHLENGTH, 
    "Path to file:  %s", lpFilename);
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
hResult = StringCchLength(tchBuffer, PATHLENGTH, nSize)
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
TextOut(hdc, 10, 10, tchBuffer, *nSize); 
```



## <a name="listing-window-properties-for-a-given-window"></a>Elenco delle proprietà della finestra per una determinata finestra

Nell'esempio seguente, la funzione [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) elenca gli identificatori di stringa delle proprietà della finestra per la finestra identificata dalla variabile hwndSubclass definita dall'applicazione. Questa funzione si basa sulla funzione di callback definita dall'applicazione WinPropProc per visualizzare le stringhe nell'area client della finestra.


```
EnumPropsEx(hwndSubclass, WinPropProc, NULL); 
 
// WinPropProc is an application-defined callback function 
// that lists a window property. 
 
BOOL CALLBACK WinPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    static int nProp = 1;    // property counter 
    TCHAR tchBuffer[BUFFER]; // expanded-string buffer 
    size_t * nSize;          // size of string in buffer 
    HDC hdc;                 // device-context handle
    HRESULT hResult; 
 
    hdc = GetDC(hwndSubclass); 
 
    // Display window property string in client area.
    hResult = StringCchPrintf(tchBuffer, BUFFER, "WinProp %d:  %s", nProp++, lpszString);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    }
    hResult = StringCchLength(tchBuffer, BUFFER, nSize);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    } 
    TextOut(hdc, 10, nProp * 20, tchBuffer, *nSize); 
 
    ReleaseDC(hwndSubclass, hdc); 
 
    return TRUE; 
} 
```



## <a name="deleting-a-window-property"></a>Eliminazione di una proprietà di finestra

Quando una finestra viene distrutta, deve eliminare tutte le proprietà della finestra impostate. L'esempio seguente usa la funzione [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) e la funzione di callback definita dall'applicazione DelPropProc per eliminare definitivamente le proprietà associate alla finestra identificata dalla variabile hwndSubclass definita dall'applicazione. Viene visualizzata anche la funzione di callback, che usa la funzione [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) .


```
case WM_DESTROY: 
 
    EnumPropsEx(hwndSubclass, DelPropProc, NULL); 
 
    PostQuitMessage(0); 
    break; 
 
// DelPropProc is an application-defined callback function 
// that deletes a window property. 
 
BOOL CALLBACK DelPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    hData = RemoveProp(hwndSubclass, lpszString); 
//
// if appropriate, free the handle hData
//
 
    return TRUE; 
}
```



 

 
