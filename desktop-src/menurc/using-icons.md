---
title: Uso delle icone
description: In questa sezione vengono forniti esempi di codice che illustrano come eseguire attività correlate alle icone.
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- risorse, icone
- icone, creazione
- icone, visualizzazione
- icone, condivisione di risorse
- creazione di icone
- visualizzazione di icone
- risorse icona di condivisione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03202c250502794d5f845bcc8c2ae263d919ea62
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327116"
---
# <a name="using-icons"></a><span data-ttu-id="5b0a4-110">Uso delle icone</span><span class="sxs-lookup"><span data-stu-id="5b0a4-110">Using Icons</span></span>

<span data-ttu-id="5b0a4-111">Gli argomenti seguenti descrivono come eseguire determinate attività correlate alle icone:</span><span class="sxs-lookup"><span data-stu-id="5b0a4-111">The following topics describe how to perform certain tasks related to icons:</span></span>

-   [<span data-ttu-id="5b0a4-112">Creazione di un'icona</span><span class="sxs-lookup"><span data-stu-id="5b0a4-112">Creating an Icon</span></span>](#creating-an-icon)
-   [<span data-ttu-id="5b0a4-113">Visualizzazione di un'icona</span><span class="sxs-lookup"><span data-stu-id="5b0a4-113">Displaying an Icon</span></span>](#displaying-an-icon)
-   [<span data-ttu-id="5b0a4-114">Risorse icona di condivisione</span><span class="sxs-lookup"><span data-stu-id="5b0a4-114">Sharing Icon Resources</span></span>](#sharing-icon-resources)

## <a name="creating-an-icon"></a><span data-ttu-id="5b0a4-115">Creazione di un'icona</span><span class="sxs-lookup"><span data-stu-id="5b0a4-115">Creating an Icon</span></span>

<span data-ttu-id="5b0a4-116">Per usare un'icona, l'applicazione deve ottenere un handle per l'icona.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-116">To use an icon, your application must get a handle to the icon.</span></span> <span data-ttu-id="5b0a4-117">L'esempio seguente illustra come creare due handle di icona diversi: uno per l'icona della domanda standard e uno per un'icona personalizzata inclusa come risorsa nel file di definizione delle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-117">The following example shows how to create two different icon handles: one for the standard question icon and one for a custom icon included as a resource in the application's resource-definition file.</span></span>


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



<span data-ttu-id="5b0a4-118">Un'applicazione deve implementare icone personalizzate come risorse e deve usare la funzione [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) o [**LoadImage,**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) anziché creare le icone in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-118">An application should implement custom icons as resources and should use the [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function, rather than create the icons at run-time.</span></span> <span data-ttu-id="5b0a4-119">Questo approccio evita le dipendenze dei dispositivi, semplifica la localizzazione e consente alle applicazioni di condividere le bitmap delle icone.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-119">This approach avoids device dependence, simplifies localization, and enables applications to share icon bitmaps.</span></span> <span data-ttu-id="5b0a4-120">Tuttavia, l'esempio seguente usa [**CreateIcon per**](/windows/desktop/api/Winuser/nf-winuser-createicon) creare un'icona personalizzata in fase di esecuzione, in base alle maschera di bit bitmap; è incluso per illustrare il modo in cui il sistema interpreta le maschera di bit bitmap delle icone.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-120">However, the following example uses [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) to create a custom icon at run-time, based on bitmap bitmasks; it is included to illustrate how the system interprets icon bitmap bitmasks.</span></span>


```
HICON hIcon3;      // icon handle 
 
// Yang icon AND bitmask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,   // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,   // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,   // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,   // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,   // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 7 
                      0xFF, 0xF0, 0x00, 0x07,   // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,   // line 9 
                      0xFF, 0xE0, 0x00, 0x03,   // line 10 
                      0xFF, 0xE0, 0x00, 0x01,   // line 11 
                      0xFF, 0xE0, 0x00, 0x01,   // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,   // line 13 
                      0xFF, 0xF0, 0x00, 0x00,   // line 14 
                      0xFF, 0xF8, 0x00, 0x00,   // line 15 
                      0xFF, 0xFC, 0x00, 0x00,   // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,   // line 17 
                      0xFF, 0xFF, 0x80, 0x00,   // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,   // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,   // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,   // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,   // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,   // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,   // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,   // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,   // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,   // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF};  // line 32 
 
// Yang icon XOR bitmask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,   // line 1 
                      0x00, 0x00, 0x00, 0x00,   // line 2 
                      0x00, 0x00, 0x00, 0x00,   // line 3 
                      0x00, 0x00, 0x00, 0x00,   // line 4 
 
                      0x00, 0x00, 0x00, 0x00,   // line 5 
                      0x00, 0x00, 0x00, 0x00,   // line 6 
                      0x00, 0x00, 0x00, 0x00,   // line 7 
                      0x00, 0x00, 0x38, 0x00,   // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,   // line 9 
                      0x00, 0x00, 0x7C, 0x00,   // line 10 
                      0x00, 0x00, 0x7C, 0x00,   // line 11 
                      0x00, 0x00, 0x38, 0x00,   // line 12 
 
                      0x00, 0x00, 0x00, 0x00,   // line 13 
                      0x00, 0x00, 0x00, 0x00,   // line 14 
                      0x00, 0x00, 0x00, 0x00,   // line 15 
                      0x00, 0x00, 0x00, 0x00,   // line 16 
 
                      0x00, 0x00, 0x00, 0x00,   // line 17 
                      0x00, 0x00, 0x00, 0x00,   // line 18 
                      0x00, 0x00, 0x00, 0x00,   // line 19 
                      0x00, 0x00, 0x00, 0x00,   // line 20 
 
                      0x00, 0x00, 0x00, 0x00,   // line 21 
                      0x00, 0x00, 0x00, 0x00,   // line 22 
                      0x00, 0x00, 0x00, 0x00,   // line 23 
                      0x00, 0x00, 0x00, 0x00,   // line 24 
 
                      0x00, 0x00, 0x00, 0x00,   // line 25 
                      0x00, 0x00, 0x00, 0x00,   // line 26 
                      0x00, 0x00, 0x00, 0x00,   // line 27 
                      0x00, 0x00, 0x00, 0x00,   // line 28 
 
                      0x00, 0x00, 0x00, 0x00,   // line 29 
                      0x00, 0x00, 0x00, 0x00,   // line 30 
                      0x00, 0x00, 0x00, 0x00,   // line 31 
                      0x00, 0x00, 0x00, 0x00};  // line 32 
 
hIcon3 = CreateIcon(hinst,    // application instance  
             32,              // icon width 
             32,              // icon height 
             1,               // number of XOR planes 
             1,               // number of bits per pixel 
             ANDmaskIcon,     // AND bitmask  
             XORmaskIcon);    // XOR bitmask 
              
```



<span data-ttu-id="5b0a4-121">Per creare l'icona, [**CreateIcon applica**](/windows/desktop/api/Winuser/nf-winuser-createicon) la tabella di verità seguente alle maschera di bit AND e XOR.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-121">To create the icon, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) applies the following truth table to the AND and XOR bitmasks.</span></span>



| <span data-ttu-id="5b0a4-122">Maschera di bit AND</span><span class="sxs-lookup"><span data-stu-id="5b0a4-122">AND bitmask</span></span> | <span data-ttu-id="5b0a4-123">Maschera di bit XOR</span><span class="sxs-lookup"><span data-stu-id="5b0a4-123">XOR bitmask</span></span> | <span data-ttu-id="5b0a4-124">Visualizza</span><span class="sxs-lookup"><span data-stu-id="5b0a4-124">Display</span></span>        |
|-------------|-------------|----------------|
| <span data-ttu-id="5b0a4-125">0</span><span class="sxs-lookup"><span data-stu-id="5b0a4-125">0</span></span>           | <span data-ttu-id="5b0a4-126">0</span><span class="sxs-lookup"><span data-stu-id="5b0a4-126">0</span></span>           | <span data-ttu-id="5b0a4-127">Black</span><span class="sxs-lookup"><span data-stu-id="5b0a4-127">Black</span></span>          |
| <span data-ttu-id="5b0a4-128">0</span><span class="sxs-lookup"><span data-stu-id="5b0a4-128">0</span></span>           | <span data-ttu-id="5b0a4-129">1</span><span class="sxs-lookup"><span data-stu-id="5b0a4-129">1</span></span>           | <span data-ttu-id="5b0a4-130">White</span><span class="sxs-lookup"><span data-stu-id="5b0a4-130">White</span></span>          |
| <span data-ttu-id="5b0a4-131">1</span><span class="sxs-lookup"><span data-stu-id="5b0a4-131">1</span></span>           | <span data-ttu-id="5b0a4-132">0</span><span class="sxs-lookup"><span data-stu-id="5b0a4-132">0</span></span>           | <span data-ttu-id="5b0a4-133">Screen</span><span class="sxs-lookup"><span data-stu-id="5b0a4-133">Screen</span></span>         |
| <span data-ttu-id="5b0a4-134">1</span><span class="sxs-lookup"><span data-stu-id="5b0a4-134">1</span></span>           | <span data-ttu-id="5b0a4-135">1</span><span class="sxs-lookup"><span data-stu-id="5b0a4-135">1</span></span>           | <span data-ttu-id="5b0a4-136">Schermata inversa</span><span class="sxs-lookup"><span data-stu-id="5b0a4-136">Reverse screen</span></span> |



 

<span data-ttu-id="5b0a4-137">Prima della chiusura, l'applicazione deve [**usare DestroyIcon per**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) eliminare qualsiasi icona creata tramite [**CreateIconIndirect.**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)</span><span class="sxs-lookup"><span data-stu-id="5b0a4-137">Before closing, your application must use [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) to destroy any icon it created by using [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect).</span></span> <span data-ttu-id="5b0a4-138">Non è necessario eliminare le icone create da altre funzioni.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-138">It is not necessary to destroy icons created by other functions.</span></span>

## <a name="displaying-an-icon"></a><span data-ttu-id="5b0a4-139">Visualizzazione di un'icona</span><span class="sxs-lookup"><span data-stu-id="5b0a4-139">Displaying an Icon</span></span>

<span data-ttu-id="5b0a4-140">L'applicazione può caricare e creare icone da visualizzare nell'area client o nelle finestre figlio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-140">Your application can load and create icons to display in the application's client area or child windows.</span></span> <span data-ttu-id="5b0a4-141">L'esempio seguente illustra come disegnare un'icona nell'area client della finestra il cui contesto di dispositivo (DC) è identificato dal *parametro hdc.*</span><span class="sxs-lookup"><span data-stu-id="5b0a4-141">The following example demonstrates how to draw an icon in the client area of the window whose device context (DC) is identified by the *hdc* parameter.</span></span>


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



<span data-ttu-id="5b0a4-142">Il sistema visualizza automaticamente le icone della classe per una finestra.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-142">The system automatically displays the class icon(s) for a window.</span></span> <span data-ttu-id="5b0a4-143">L'applicazione può assegnare icone di classe durante la registrazione di una classe finestra.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-143">Your application can assign class icons while registering a window class.</span></span> <span data-ttu-id="5b0a4-144">L'applicazione può sostituire un'icona di classe usando la [**funzione SetClassLong.**](/windows/desktop/api/winuser/nf-winuser-setclasslonga)</span><span class="sxs-lookup"><span data-stu-id="5b0a4-144">Your application can replace a class icon by using the [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) function.</span></span> <span data-ttu-id="5b0a4-145">Questa funzione modifica le impostazioni predefinite della finestra per tutte le finestre di una determinata classe.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-145">This function changes the default window settings for all windows of a given class.</span></span> <span data-ttu-id="5b0a4-146">L'esempio seguente sostituisce un'icona della classe con l'icona il cui identificatore di risorsa è 480.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-146">The following example replaces a class icon with the icon whose resource identifier is 480.</span></span>


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLongPtr(hwnd,          // window handle 
    GCLP_HICON,              // changes icon 
    (LONG_PTR) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



<span data-ttu-id="5b0a4-147">Per altre informazioni sulle classi finestra, vedere [Classi finestra](/windows/desktop/winmsg/window-classes).</span><span class="sxs-lookup"><span data-stu-id="5b0a4-147">For more information about window classes, see [Window Classes](/windows/desktop/winmsg/window-classes).</span></span>

## <a name="sharing-icon-resources"></a><span data-ttu-id="5b0a4-148">Risorse delle icone di condivisione</span><span class="sxs-lookup"><span data-stu-id="5b0a4-148">Sharing Icon Resources</span></span>

<span data-ttu-id="5b0a4-149">Il codice seguente usa le funzioni [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)e [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex)e diverse funzioni di risorsa per creare un handle di icona basato sui dati dell'icona da un altro file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-149">The following code uses the functions [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), and [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), and several of the resource functions, to create an icon handle based on icon data from another executable file.</span></span> <span data-ttu-id="5b0a4-150">Visualizza quindi l'icona in una finestra.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-150">Then, it displays the icon in a window.</span></span>

<span data-ttu-id="5b0a4-151">**Avviso di sicurezza:** [**L'uso non corretto di LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la DLL errata.</span><span class="sxs-lookup"><span data-stu-id="5b0a4-151">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="5b0a4-152">Per informazioni su come caricare correttamente le DLL con versioni diverse di Windows, vedere la documentazione di **LoadLibrary.**</span><span class="sxs-lookup"><span data-stu-id="5b0a4-152">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```
HICON hIcon1;       // icon handle 
HINSTANCE hExe;     // handle to loaded .EXE file 
HRSRC hResource;    // handle to FindResource  
HRSRC hMem;         // handle to LoadResource 
BYTE *lpResource;   // pointer to resource data  
int nID;            // ID of resource that best fits current screen 
 
HDC hdc;        // handle to display context 
 
// Load the file from which to copy the icon. 
// Note: LoadLibrary should have a fully explicit path.
//
hExe = LoadLibrary("myapp.exe");
if (hExe == NULL)
{
    //Error loading module -- fail as securely as possible
    return;
}
 
 
// Find the icon directory whose identifier is 440. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(440), 
    RT_GROUP_ICON); 
 
// Load and lock the icon directory. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Get the identifier of the icon that is most appropriate 
// for the video display. 
 
nID = LookupIconIdFromDirectoryEx((PBYTE) lpResource, TRUE, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Find the bits for the nID icon. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(nID), 
    MAKEINTRESOURCE(RT_ICON)); 
 
// Load and lock the icon. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Create a handle to the icon. 
 
hIcon1 = CreateIconFromResourceEx((PBYTE) lpResource, 
    SizeofResource(hExe, hResource), TRUE, 0x00030000, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Draw the icon in the client area. 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



 

 
